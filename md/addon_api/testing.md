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
```

- `enableGameTests = false` leaves out Fabric's server game tests, the add-on is client-only.
- `LB_BASIC_MODE` keeps Minecraft's own menus, which the test API navigates, instead of the client's web interface. The HUD stays the client's.
- `fabric.noGui` stops Fabric Loader from waiting on an error dialog nobody sees.
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

### Running

```sh
./gradlew runClientGameTest
```

The game needs a display. Without one, for example in CI, run it under Xvfb. Minecraft asks for an sRGB framebuffer, which Xvfb's GLX does not offer, so SDL has to use EGL (`libegl1` on Debian and Ubuntu):

```sh
SDL_VIDEO_FORCE_EGL=1 xvfb-run -a -s "-screen 0 1280x720x24" ./gradlew runClientGameTest
```

Screenshots land in `build/run/clientGameTest/screenshots/`.
