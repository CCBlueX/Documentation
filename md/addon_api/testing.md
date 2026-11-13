## Testing

Fabric's client game tests start the real game with the client and the add-on, and drive it from code: create a world, enable modules, run commands, take screenshots. [Extras](https://github.com/CCBlueX/LiquidBounce-Addon-Extras) runs every one of its modules this way, LiquidBounce tests itself the same way.

### Setup

Fabric Loom creates a separate `gametest` source set, a mod of its own that is never part of the add-on's jar. In `build.gradle.kts`:

```kotlin
fabricApi {
    configureTests {
        createSourceSet = true
        modId = "example-addon-gametest"
        enableGameTests = false
    }
}

loom.runs.named("clientGameTest") {
    environmentVars.put("LB_BASIC_MODE", "true")
    systemProperties.put("fabric.noGui", "true")
    systemProperties.put(
        "net.ccbluex.liquidbounce.browser.libraries",
        gradle.gradleUserHomeDir.resolve("liquidbounce-gametest/mcef").path,
    )
}

tasks.named("runClientGameTest") {
    timeout = java.time.Duration.ofMinutes(20)
}
```

- `enableGameTests = false` leaves out Fabric's server game tests, the add-on is client-only.
- `LB_BASIC_MODE` keeps Minecraft's own menus, which the test API navigates, instead of the client's web interface. The HUD stays the client's.
- `fabric.noGui` stops Fabric Loader from waiting on an error dialog nobody sees.
- The `timeout` ends a game that hangs, for example one that never finds a renderer.
- The run directory is wiped before every run. The browser the client downloads on its first start (about 140 MB) is kept outside of it through `net.ccbluex.liquidbounce.browser.libraries`.

`src/gametest/resources/fabric.mod.json` declares the test:

```json
{
  "schemaVersion": 1,
  "id": "example-addon-gametest",
  "version": "1.0.0",
  "name": "Example Addon Game Tests",
  "environment": "client",
  "entrypoints": {
    "fabric-client-gametest": [
      "com.example.addon.gametest.ExampleGameTest"
    ]
  },
  "depends": {
    "example-addon": "*",
    "fabric-client-gametest-api-v1": "*"
  }
}
```

### Writing a test

```kotlin
class ExampleGameTest : FabricClientGameTest {

    override fun runTest(context: ClientGameTestContext) {
        context.waitFor({ BrowserBackendManager.backend?.isInitialized == true }, 20 * 120)

        context.worldBuilder().create().use { world ->
            world.connection.waitForChunksRender()

            val module = requireNotNull(ModuleManager["JumpCounter"]) { "JumpCounter is not registered" }
            context.client { module.enabled = true }
            context.waitTicks(20)
            context.takeScreenshot("JumpCounter")
            context.client { module.enabled = false }

            context.client { CommandManager.execute("greet") }
            context.waitTicks(2)
        }
    }

}

// The context's lambdas declare a throwable type Kotlin cannot infer.
private fun <T> ClientGameTestContext.client(block: (Minecraft) -> T): T =
    computeOnClient<T, RuntimeException> { block(it) }
```

- The test runs on its own thread. Anything that touches the game or the client goes through `computeOnClient` or `runOnClient`, the server through `world.server`.
- Waiting for the browser first lets the client finish starting.
- `ModuleManager[name]` finds a module, `CommandManager.execute` runs a command without the prefix.
- An exception fails the run. Extras also collects every logged error and fails on them, which catches problems inside handlers that the client only logs.

### Tests on the game test server

A server game test plays on a real Paper server with an anticheat watching. The test joins under a bot name of its own and gets worlds of its own, from any seed, where it runs commands such as `summon` or `fill`. An attempt fails when the server objects to what the client did more than 5 times (flags from the anticheat, movements Paper corrected or client errors; a setback after a flag does not count) and fails at once on a kick, a refused command or a lost connection. A failed test runs again up to 2 times under a new name. A test can change both limits. The server and the harness are [CCBlueX Gametest](https://github.com/CCBlueX/gametest). Its [protocol](https://github.com/CCBlueX/gametest/blob/main/docs/protocol.md) is documented, so a test that does not use the harness can play there too.

LiquidBounce publishes `net.ccbluex:liquidbounce-gametest` in the same versions as the client. It brings the harness with it:

```kotlin
dependencies {
    "gametestImplementation"("net.ccbluex:liquidbounce-gametest:${libs.versions.liquidbounce.get()}")
}
```

In `fabric.mod.json`, depend on `liquidbounce-gametest-harness` and list `net.ccbluex.gametest.harness.ResultsGameTest` after every test. It fails the run when a server test failed:

```json
"entrypoints": {
  "fabric-client-gametest": [
    "com.example.addon.gametest.AutoShearerGameTest",
    "net.ccbluex.gametest.harness.ResultsGameTest"
  ]
},
"depends": {
  "example-addon": "*",
  "liquidbounce-gametest-harness": "*",
  "fabric-client-gametest-api-v1": "*"
}
```

```kotlin
class AutoShearerGameTest : ServerGameTest({
    val module = requireNotNull(ModuleManager["AutoShearer"]) { "AutoShearer is not registered" }
    give("minecraft:shears")
    summon("minecraft:sheep", origin.south(2), "{NoAI:1b}")
    enable(module)
    awaitServer("entity @e[type=minecraft:sheep,nbt={Sheared:1b}]")
    disable(module)
})
```

- The class a test extends says where it plays. `ServerGameTest` plays on the game test server with the chosen anticheat watching. `SingleplayerGameTest` plays on the client's integrated server with the same scope and commands. `ClientGameTest` plays without a world.
- Every test waits until the client has started, runs with every module but the HUD turned off and turns the modules that ran before back on afterwards.
- The bot starts at `origin` on a superflat world, looking south. `ServerGameTest(TestWorld.generated(seed)) { ... }` plays on real terrain from a seed.
- `give`, `summon`, `setBlock`, `fill` and `run(command)` run as the server console and reach only the test's own worlds and bot. `awaitServer` waits until an `execute if` condition holds, `query` reads the answer of a command. Check on the server what the client did, not only on the client.
- `enable(module)` and `disable(module)` switch a module, `command(line)` runs a client command (it never reaches the server) and `module.setting<T>(name)` finds a setting by name. `configure(module, "Name" to value)` sets settings by name. A text sets a setting that holds something else the way a config does, such as a mode by its name.
- A test that only checks what the client receives and does extends `SingleplayerGameTest`, or `ClientGameTest` when it needs no world.

The [gametest-harness skill](https://github.com/CCBlueX/gametest/blob/main/skills/gametest-harness/SKILL.md) teaches a coding agent the harness API and the rules a test follows.

### Picking the server and the anticheat

| Variable | Meaning |
|---|---|
| `GAMETEST_API_TOKEN` | The API token from your [account page](https://liquidbounce.net/account). Needed for the public server `test.ccbluex.net`. |
| `GAMETEST_SERVER_ANTICHEAT` | Which anticheat watches the bot. `grim` when it is not set. |
| `GAMETEST_SERVER_ADDRESS` | A server of your own, such as `localhost:25565`. It needs no token. |

Without a token or an address, the server tests are skipped. When the bot logs in to `test.ccbluex.net`, the harness gets a one-time ticket for it from the LiquidBounce API with your token, and the bot joins with that ticket. Every bot is logged with the account behind its token, so please use the public server fairly.

| `GAMETEST_SERVER_ANTICHEAT` | What watches the bot |
|---|---|
| `vanilla` | Only Paper's own movement checks |
| `grim` | Grim |
| `intave` | Intave |
| `vulcan` | Vulcan |
| `matrix` | Matrix |
| `spartan` | Spartan |
| `mx` | MX, which only checks aim in fights |
| `anticheataddition` | AntiCheatAddition, without movement checks |
| `fairplay` | FairPlay, without movement checks |

To run the server yourself, start it from the [repository](https://github.com/CCBlueX/gametest) with `docker compose up --build` and point `GAMETEST_SERVER_ADDRESS` at it. It downloads Grim and Intave; the paid anticheats are only on the public server.

When a server test fails, the log names every objection: `FLAG` and `SETBACK` come from the anticheat, `FAILMOVE` and `KICK` from Paper. `build/run/clientGameTest/gametest/<Test>.log` has every message the test sent to the server and got back.

### Running

```sh
./gradlew runClientGameTest
```

The game needs a display. Without one, for example in CI, run it under Xvfb. Minecraft asks for an sRGB framebuffer, which Xvfb's GLX does not offer, so SDL has to use EGL (`libegl1` on Debian and Ubuntu):

```sh
SDL_VIDEO_FORCE_EGL=1 xvfb-run -a -s "-screen 0 1280x720x24" ./gradlew runClientGameTest
```

Screenshots land in `build/run/clientGameTest/screenshots/`.

In GitHub Actions, give the job your API token as a secret and run the tests once per anticheat. Give the job a `timeout-minutes` and `runClientGameTest` a Gradle `timeout`, so a game that hangs does not hold the runner:

```yaml
gametest:
  runs-on: ubuntu-latest
  timeout-minutes: 30
  strategy:
    fail-fast: false
    matrix:
      anticheat: [vanilla, grim, intave]
  steps:
    # checkout, Java and Gradle as in the build job
    - run: sudo apt-get update && sudo apt-get install -y libegl1 libegl-mesa0
    - run: xvfb-run -a -s "-screen 0 1280x720x24" ./gradlew runClientGameTest
      env:
        SDL_VIDEO_FORCE_EGL: 1
        GAMETEST_API_TOKEN: ${{ secrets.LIQUIDBOUNCE_API_TOKEN }}
        GAMETEST_SERVER_ANTICHEAT: ${{ matrix.anticheat }}
```

---

*Last updated: 2026-11-12, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/b7185570b/build.gradle.kts)*
