## Getting Started

Add-ons are Fabric mods that compile against LiquidBounce itself. They build on the same classes as the client's own modules, commands and HUD components, can ship Mixins and access wideners, and are loaded by the client while it starts. For small features, the [Script API](/docs/script-api/installation) is the simpler option.

Add-ons are written in Kotlin or Java. The examples in this section are Kotlin, [Using Java](/docs/add-on-api/developers/using-java) covers where Java differs. Minecraft's classes carry Mojang's official names, there is no other mapping layer.

### Requirements

- JDK 25
- Git
- An IDE with Kotlin support, for example [IntelliJ IDEA](https://www.jetbrains.com/idea/)

### Creating the project

Start from the [add-on template](https://github.com/CCBlueX/LiquidBounce-Addon-Template): click **Use this template** on GitHub, or clone it.

```sh
git clone --depth 1 https://github.com/CCBlueX/LiquidBounce-Addon-Template my-addon
```

Then rename the example:

| File                                               | What to change                                                                              |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| `settings.gradle.kts`                              | `rootProject.name`                                                                          |
| `gradle.properties`                                | `maven_group`, `archives_base_name`                                                         |
| `src/main/resources/fabric.mod.json`               | `id`, `name`, `description`, `authors`, `contact`, the entrypoint class                     |
| `src/main/resources/example-addon.mixins.json`     | file name and `package`, and `mixins` in `fabric.mod.json`                                  |
| `src/main/resources/example-addon.accesswidener`   | file name, `accessWidener` in `fabric.mod.json` and `loom.accessWidenerPath` in `build.gradle.kts` |
| `src/main/resources/resources/example-addon/`      | folder name, which must match the add-on id, and the `icon` path                            |
| `src/main/kotlin/com/example/addon/`               | package name                                                                                |
| `src/main/java/com/example/addon/mixin/`           | package name                                                                                |

The build setup is explained in [Project Setup](/docs/add-on-api/developers/project-setup), the manifest in [Manifest and Lifecycle](/docs/add-on-api/developers/manifest-and-lifecycle).

### Writing a module

A module is a `ClientModule`. Its [settings](/docs/add-on-api/developers/settings) and [event handlers](/docs/add-on-api/developers/events) are properties. This one counts the player's jumps and reports every tenth:

```kotlin
package com.example.addon.modules

import com.example.addon.ExampleCategories
import net.ccbluex.liquidbounce.event.events.PlayerJumpEvent
import net.ccbluex.liquidbounce.event.handler
import net.ccbluex.liquidbounce.features.module.ClientModule
import net.ccbluex.liquidbounce.utils.client.chat

object ModuleJumpCounter : ClientModule("JumpCounter", ExampleCategories.EXAMPLE) {

    private val every by int("Every", 10, 1..100, "jumps")

    private var jumps = 0

    override fun onEnabled() {
        jumps = 0
    }

    @Suppress("unused")
    private val jumpHandler = handler<PlayerJumpEvent> {
        jumps++

        if (jumps % every == 0) {
            chat("You jumped $jumps times.")
        }
    }

}
```

The handler only runs while the module is enabled and the player is in a world. `chat` prints to the chat without sending anything to the server.

### Registering the module

Modules are registered by the entrypoint, the class named under `liquidbounce` in `fabric.mod.json`:

```kotlin
package com.example.addon

import com.example.addon.modules.ModuleJumpCounter
import net.ccbluex.liquidbounce.features.addon.LiquidBounceAddon

class ExampleAddon : LiquidBounceAddon() {

    override val categories = listOf(ExampleCategories.EXAMPLE)

    override fun onInitialize() {
        registerModules(ModuleJumpCounter)
    }

}
```

`categories` registers the template's **Example** category. A module can also go into a built-in category from `ModuleCategories`, see [Categories](/docs/add-on-api/developers/categories).

### Adding a description

The ClickGUI shows a description for every module and setting. They come from `src/main/resources/resources/<id>/lang/en_us.json`:

```json
{
  "liquidbounce.module.jumpCounter.description": "Counts your jumps.",
  "liquidbounce.module.jumpCounter.every.description": "Jumps between two messages."
}
```

A module without an `en_us` description logs a warning when it is registered. The key format is explained in [Translations](/docs/add-on-api/developers/translations).

### Running and building

```sh
./gradlew runClient
```

starts Minecraft with LiquidBounce and the add-on. Join a world, open the ClickGUI with **RIGHT SHIFT** and find **JumpCounter** under **Example**. `.addon list` lists the add-on, `.addon info <id>` shows what it registered.

```sh
./gradlew build
```

writes the add-on to `build/libs/`, as `example-addon-1.0.0+26.3.jar` next to a `-sources` jar. Install the jar like any other mod, as an [additional mod in LiquidLauncher](/docs/get-started/liquidlauncher#client) or in the *mods* folder of a [manual installation](/docs/get-started/manual-installation). To offer it on the Marketplace, see [Publishing](/docs/add-on-api/developers/publishing).

### Examples

- [LiquidBounce-Addon-Template](https://github.com/CCBlueX/LiquidBounce-Addon-Template): the starting point, with a module, a command, a category and a Mixin.
- [LiquidBounce-Addon-Extras](https://github.com/CCBlueX/LiquidBounce-Addon-Extras): modules in Kotlin and Java side by side, each covered by a game test.
- [LiquidBounce-Addon-ScriptAPI](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI): a larger add-on with Mixins into LiquidBounce.
- [LiquidBounce-Addon-Wry](https://github.com/CCBlueX/LiquidBounce-Addon-Wry): a [browser backend](/docs/add-on-api/developers/browser-backends).
