## Creating Modules

A module is a `ClientModule`. It shows up in the ClickGUI, can be toggled and bound like a built-in one, keeps its settings in the client's module config, and runs its event handlers while it is enabled.

### Declaring a module

In Kotlin a module is usually an `object`, in Java a class that is instantiated once.

```kotlin
object ModuleHitCounter : ClientModule("HitCounter", ModuleCategories.COMBAT) {

    private val announce by boolean("Announce", true)

    private var hits = 0

    override val tag: String
        get() = hits.toString()

    init {
        literalDescription { "Counts the hits you land." }
    }

    override fun onEnabled() {
        hits = 0
    }

    override fun onDisabled() {
        if (announce) {
            chat(regular("You landed ").append(variable(hits.toString())).append(regular(" hits.")), this)
        }
    }

    @Suppress("unused")
    private val attackHandler = handler<AttackEntityEvent> {
        hits++
        EventManager.callEvent(RefreshArrayListEvent)
    }

}
```

The constructor takes:

| Property          | Description                                                                                              | Required | Type                     | Default     |
|-------------------|----------------------------------------------------------------------------------------------------------|----------|--------------------------|-------------|
| name              | Name of the module. Unique regardless of case, also the base of its [translation keys](/docs/add-on-api/developers/translations). | Yes | `String`       |             |
| category          | The [category](/docs/add-on-api/developers/categories) it is filed under.                                           | Yes      | `ModuleCategory`         |             |
| bind              | Default key, for example `InputConstants.KEY_C`.                                                         | No       | `Int`                    | unbound     |
| bindAction        | What the key does: `TOGGLE`, `HOLD` (enabled while held) or `SMART` (hold or toggle, by how the key is pressed). | No | `InputBind.BindAction` | `TOGGLE` |
| state             | Whether the module starts enabled.                                                                       | No       | `Boolean`                | `false`     |
| notActivatable    | The module cannot be toggled. Its handlers run whenever the player is in a world. For modules that only hold settings. | No | `Boolean` | `false` |
| disableActivation | Enabling runs `onEnabled()`, but the module does not stay enabled, like the ClickGUI module.            | No       | `Boolean`                | `notActivatable` |
| disableOnQuit     | Disabled when the player leaves the server.                                                              | No       | `Boolean`                | `false`     |
| aliases           | Former names, stored settings under one of them still load.                                              | No       | `List<String>`           | `[]`        |
| hide              | Hidden from the module list on the HUD by default.                                                       | No       | `Boolean`                | `false`     |

```kotlin
object ModuleZoomHold : ClientModule(
    "ZoomHold",
    ModuleCategories.RENDER,
    bind = InputConstants.KEY_C,
    bindAction = InputBind.BindAction.HOLD,
    disableOnQuit = true,
)
```

Register modules from the add-on's `onInitialize()`:

```kotlin
registerModules(ModuleHitCounter, ModuleZoomHold)
```

A name that is already taken, or a category that is not registered, fails the add-on.

### Hooks

| Function            | Called                                                                                   |
|---------------------|------------------------------------------------------------------------------------------|
| `onEnabled()`       | When the module is enabled. Only while the player is in a world; a module that was enabled from the config gets it when the player first joins one. |
| `onDisabled()`      | When the module is disabled.                                                             |
| `onRegistration()`  | Once, when `registerModules` adds the module.                                            |
| `enabledEffect()`   | A `suspend` function launched after the module was enabled, cancelled when it is disabled. |

Everything else the module does happens in [event handlers](/docs/add-on-api/developers/events). They run while `running` is true, that is while the module is enabled and the player is in a world.

### Properties

| Property   | Type                         | Description                                                                             |
|------------|------------------------------|-----------------------------------------------------------------------------------------|
| `enabled`  | `Boolean`                    | Read or set the state. Setting it runs the hooks as if the player had toggled it.       |
| `running`  | `Boolean`                    | Whether handlers run right now.                                                         |
| `hidden`   | `Boolean`                    | Hidden from the module list on the HUD.                                                 |
| `tag`      | `String?`                    | Shown next to the name in the module list. Override it, or pass a setting to `tagBy(value)`. |
| `bind`     | `InputBind`                  | The current key binding.                                                                |
| `settings` | `Map<String, Value<*>>`      | The module's settings by name.                                                          |
| `category` | `ModuleCategory`             | The category from the constructor.                                                      |

The module list only reads `tag` again after a `RefreshArrayListEvent`, so call `EventManager.callEvent(RefreshArrayListEvent)` when an overridden `tag` changes. `tagBy(value)` does that by itself.

Modules have the usual Minecraft shortcuts: `mc`, `player`, `world`, `network`, `interaction` and `inGame`. `player` and `world` are only safe to use while the player is in a world, which is always the case inside handlers.

### Output

```kotlin
chat("Plain text")
chat(regular("Found ").append(variable("3")).append(regular(" chests")), this)
notification("Example", "Done", NotificationEvent.Severity.SUCCESS)
```

- `chat` prints to the chat with the client's prefix, nothing is sent to the server. Passing the module makes each message replace the module's previous one instead of adding a line.
- `regular`, `variable`, `highlight`, `warning` and `markAsError` color text the way the client's own messages are colored.
- `notification` shows a notification with a title, a message and a `NotificationEvent.Severity` (`INFO`, `SUCCESS`, `ERROR`, `ENABLED`, `DISABLED`).
- `message(key, args)` returns the translation of `liquidbounce.module.<module>.messages.<key>`, see [Translations](/docs/add-on-api/developers/translations).

### Modes

A module with alternative behaviors declares them as modes. Each mode is a `Mode` with its own settings and handlers, which only run while that mode is selected and the module is enabled:

```kotlin
object ModuleJumpBoost : ClientModule("JumpBoost", ModuleCategories.MOVEMENT) {

    private val mode = choices("Mode", Motion, Delayed)

    private object Motion : Mode("Motion") {

        override val parent get() = mode

        private val factor by float("Factor", 1.2f, 1f..2f)

        @Suppress("unused")
        private val jumpHandler = handler<PlayerJumpEvent> { event ->
            event.motion *= factor
        }

    }

    private object Delayed : Mode("Delayed") {

        override val parent get() = mode

        private val delay by int("Delay", 2, 1..10, "ticks")

        @Suppress("unused")
        private val tickHandler = tickHandler {
            if (player.onGround()) {
                waitTicks(delay)
                player.jumpFromGround()
            }
        }

    }

}
```

`choices` selects the first mode by default. See [`choices`](/docs/add-on-api/developers/settings) for the other forms.

### Descriptions

The ClickGUI shows a description for the module and each setting. They come from the add-on's [translations](/docs/add-on-api/developers/translations) under `liquidbounce.module.<module>.description`. `literalDescription { "..." }` sets a fixed text instead. A module with neither logs a warning when it is registered.
