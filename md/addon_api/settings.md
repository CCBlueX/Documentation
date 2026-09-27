## Settings

Settings are declared on a `ValueGroup`: a module, a [mode](/docs/add-on-api/developers/creating-modules#modes), a nested group, or a group passed to the add-on's `config(...)`. They show up in the ClickGUI and are stored with the client's configs.

In Kotlin, `by` reads the setting like a plain property. Without `by` the property holds the `Value`, which is needed for its modifiers or to set it from code. In Java, fields hold the `Value` and are read with `get()`, see [Using Java](/docs/add-on-api/developers/using-java).

```kotlin
private val range by float("Range", 4.2f, 1f..6f, "blocks") // Float
private val rangeValue = float("Range", 4.2f, 1f..6f, "blocks") // Value<Float>
```

The name is the key in the config file and part of the setting's [translation key](/docs/add-on-api/developers/translations). Renaming a setting loses its stored value, unless the old name goes into `aliases` where the builder has that parameter. A module already has settings named `Enabled`, `Bind` and `Hidden`.

In Kotlin, a property holding a setting cannot be called `name`, `tag`, `key` or anything else `Value` or `ClientModule` already declares.

### Builder summary

#### `boolean(name, default, aliases)`
Creates an on/off setting. Java: `bool`. <br>

| Property | Description                                | Required | Type           | Default |
|----------|--------------------------------------------|----------|----------------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String`       |         |
| default  | Initial value.                             | Yes      | `Boolean`      |         |
| aliases  | Former names.                              | No       | `List<String>` | `[]`    |

**Example:**
```kotlin
private val sneak by boolean("Sneak", true)
```

<hr>

#### `int(name, default, range, suffix, aliases)`
Creates an integer setting between the bounds of `range`. Java: `integer`, also as `integer(name, default, min, max, suffix)`. <br>

| Property | Description                                                  | Required | Type           | Default |
|----------|--------------------------------------------------------------|----------|----------------|---------|
| name     | Name under which the setting is displayed.                   | Yes      | `String`       |         |
| default  | Initial value.                                               | Yes      | `Int`          |         |
| range    | Lowest and highest value.                                    | Yes      | `IntRange`     |         |
| suffix   | Displayed next to the value to describe its unit.            | No       | `String`       | `""`    |
| aliases  | Former names.                                                | No       | `List<String>` | `[]`    |

**Example:**
```kotlin
private val delay by int("Delay", 10, 0..40, "ticks")
```

<hr>

#### `float(name, default, range, suffix, aliases)`
Creates a floating-point setting between the bounds of `range`. Java: `floating`, also as `floating(name, default, min, max, suffix)`. <br>

| Property | Description                                                  | Required | Type                               | Default |
|----------|--------------------------------------------------------------|----------|------------------------------------|---------|
| name     | Name under which the setting is displayed.                   | Yes      | `String`                           |         |
| default  | Initial value.                                               | Yes      | `Float`                            |         |
| range    | Lowest and highest value.                                    | Yes      | `ClosedFloatingPointRange<Float>`  |         |
| suffix   | Displayed next to the value to describe its unit.            | No       | `String`                           | `""`    |
| aliases  | Former names.                                                | No       | `List<String>`                     | `[]`    |

**Example:**
```kotlin
private val range by float("Range", 4.2f, 1f..6f, "blocks")
```

<hr>

#### `intRange(name, default, range, suffix, aliases)`
Creates a setting with a low and a high integer, both between the bounds of `range`. <br>

| Property | Description                                                  | Required | Type           | Default |
|----------|--------------------------------------------------------------|----------|----------------|---------|
| name     | Name under which the setting is displayed.                   | Yes      | `String`       |         |
| default  | Initial low and high value.                                  | Yes      | `IntRange`     |         |
| range    | Lowest and highest value.                                    | Yes      | `IntRange`     |         |
| suffix   | Displayed next to the value to describe its unit.            | No       | `String`       | `""`    |
| aliases  | Former names.                                                | No       | `List<String>` | `[]`    |

**Example:**
```kotlin
private val cps by intRange("CPS", 8..12, 1..20)
```

<hr>

#### `floatRange(name, default, range, suffix, aliases)`
Creates a setting with a low and a high floating-point value, both between the bounds of `range`. <br>

| Property | Description                                                  | Required | Type                               | Default |
|----------|--------------------------------------------------------------|----------|------------------------------------|---------|
| name     | Name under which the setting is displayed.                   | Yes      | `String`                           |         |
| default  | Initial low and high value.                                  | Yes      | `ClosedFloatingPointRange<Float>`  |         |
| range    | Lowest and highest value.                                    | Yes      | `ClosedFloatingPointRange<Float>`  |         |
| suffix   | Displayed next to the value to describe its unit.            | No       | `String`                           | `""`    |
| aliases  | Former names.                                                | No       | `List<String>`                     | `[]`    |

**Example:**
```kotlin
private val jitter by floatRange("Jitter", 0.5f..1.5f, 0f..5f, "deg")
```

<hr>

#### `text(name, default)`
Creates a text setting. <br>

| Property | Description                                | Required | Type     | Default |
|----------|--------------------------------------------|----------|----------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String` |         |
| default  | Initial value.                             | Yes      | `String` |         |

**Example:**
```kotlin
private val message by text("Message", "Hello")
```

<hr>

#### `textList(name, default)`
Creates a list of texts the player can add to and remove from. <br>

| Property | Description                                | Required | Type                        | Default |
|----------|--------------------------------------------|----------|-----------------------------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String`                    |         |
| default  | Initial entries.                           | Yes      | `MutableCollection<String>` |         |

**Example:**
```kotlin
private val messages by textList("Messages", mutableListOf("Hello", "Hi"))
```

<hr>

#### `regex(name, default)`
Creates a regular expression setting, edited as text. <br>

| Property | Description                                | Required | Type     | Default |
|----------|--------------------------------------------|----------|----------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String` |         |
| default  | Initial value.                             | Yes      | `Regex`  |         |

**Example:**
```kotlin
private val filter by regex("Filter", Regex("^[a-z0-9_]+$"))
```

<hr>

#### `regexList(name, default)`
Creates a list of regular expressions. <br>

| Property | Description                                | Required | Type                       | Default |
|----------|--------------------------------------------|----------|----------------------------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String`                   |         |
| default  | Initial entries.                           | Yes      | `MutableCollection<Regex>` |         |

**Example:**
```kotlin
private val ignored by regexList("Ignored", mutableListOf(Regex("\\[Ad].*")))
```

<hr>

#### `color(name, default)`
Creates a color setting with alpha. See [Color4b](/docs/add-on-api/developers/rendering#colors). <br>

| Property | Description                                | Required | Type      | Default |
|----------|--------------------------------------------|----------|-----------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String`  |         |
| default  | Initial value.                             | Yes      | `Color4b` |         |

**Example:**
```kotlin
private val fill by color("Fill", Color4b(0, 160, 255, 120))
```

<hr>

#### `key(name, default)`
Creates a setting holding a single key, as `InputConstants.Key`. <br>

| Property | Description                                                         | Required | Type                             | Default   |
|----------|---------------------------------------------------------------------|----------|----------------------------------|-----------|
| name     | Name under which the setting is displayed.                          | Yes      | `String`                         |           |
| default  | Initial key, as a key code or an `InputConstants.Key`.              | No       | `Int` or `InputConstants.Key`    | unbound   |

**Example:**
```kotlin
private val openKey by key("OpenKey", InputConstants.KEY_R)
```

<hr>

#### `bind(name, default)`
Creates a key binding like the one every module has, with an action (`TOGGLE`, `HOLD`, `SMART`) and modifier keys. Check it against key events with `InputBind.matchesKeyPress(event)` and `matchesKeyRelease(event)`. <br>

| Property | Description                                                  | Required | Type                  | Default |
|----------|--------------------------------------------------------------|----------|-----------------------|---------|
| name     | Name under which the setting is displayed.                   | Yes      | `String`              |         |
| default  | Initial binding, as a key code (action `TOGGLE`) or an `InputBind`. | No | `Int` or `InputBind` | unbound |

**Example:**
```kotlin
private val boostBind by bind("BoostBind", InputBind(InputConstants.Type.KEYBOARD, InputConstants.KEY_V, InputBind.BindAction.HOLD))
```

<hr>

#### `enumChoice(name, default, aliases)`
Creates a single choice between the constants of an enum. The enum implements `Tagged`, whose `tag` is the name shown for each constant. Java: `enumChoice(name, default)`. Any other set of `Tagged` values works with `enumChoice(name, default, choices)`. <br>

| Property | Description                                | Required | Type           | Default |
|----------|--------------------------------------------|----------|----------------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String`       |         |
| default  | Initial choice.                            | Yes      | enum `T : Tagged` |      |
| aliases  | Former names.                              | No       | `List<String>` | `[]`    |

**Example:**
```kotlin
enum class Target(override val tag: String) : Tagged {
    PLAYERS("Players"),
    MOBS("Mobs"),
    ANIMALS("Animals"),
}

private val target by enumChoice("Target", Target.PLAYERS)
```

<hr>

#### `multiEnumChoice(name, vararg default, canBeNone)`
Creates a choice of any number of an enum's constants. The value is a `MutableSet`. `default` can also be an `Iterable` or an `EnumSet`, the `EnumSet` form takes `choices` to offer only some constants. Java: `multiEnumChoice(name, type, default, canBeNone)` with the enum's `Class`. <br>

| Property  | Description                                  | Required | Type                | Default |
|-----------|----------------------------------------------|----------|---------------------|---------|
| name      | Name under which the setting is displayed.   | Yes      | `String`            |         |
| default   | Initially selected constants.                | No       | enum `T : Tagged`   | none    |
| canBeNone | Whether the player may deselect every entry. | No       | `Boolean`           | `true`  |

**Example:**
```kotlin
enum class Part(override val tag: String) : Tagged {
    HEAD("Head"),
    BODY("Body"),
    FEET("Feet"),
}

private val parts by multiEnumChoice("Parts", Part.HEAD, Part.BODY)
```

<hr>

#### `easing(name, default)`
Creates a choice of an `Easing` curve. `Easing.transform(x)` maps progress from 0 to 1. <br>

| Property | Description                                | Required | Type     | Default |
|----------|--------------------------------------------|----------|----------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String` |         |
| default  | Initial curve.                             | Yes      | `Easing` |         |

**Example:**
```kotlin
private val transition by easing("Transition", Easing.QUAD_OUT)
```

<hr>

#### `curve(name) { ... }`
Creates a curve the player shapes by moving points. Keep the `CurveValue` and call `transform(x)` to read the curve at `x`. The builder takes the axes as `"Label" x range` and `"Label" y range`, the initial `points(...)` (at least two, inside the axes) and optionally `tension` (0 to 1, default 0.4). <br>

| Property | Description                                | Required | Type                         | Default |
|----------|--------------------------------------------|----------|------------------------------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String`                     |         |
| block    | Builder for axes, points and tension.      | Yes      | `CurveValue.Builder.() -> Unit` |      |

**Example:**
```kotlin
private val falloff = curve("Falloff") {
    "Distance" x 0f..8f
    "Strength" y 0f..1f
    points(Vector2f(0f, 1f), Vector2f(8f, 0f))
}

val strength = falloff.transform(3f)
```

<hr>

#### `file(name, default, dialogMode, supportedExtensions)`
Creates a file setting with a button that opens the system's file dialog. Paths inside the LiquidBounce folder are stored relative to it. <br>

| Property            | Description                                                                    | Required | Type             | Default                |
|---------------------|--------------------------------------------------------------------------------|----------|------------------|------------------------|
| name                | Name under which the setting is displayed.                                     | Yes      | `String`         |                        |
| default             | Initial file.                                                                  | No       | `File?`          | the LiquidBounce folder |
| dialogMode          | `OPEN_FILE`, `SAVE_FILE` or `OPEN_DIRECTORY`.                                  | No       | `FileDialogMode` | `OPEN_FILE`            |
| supportedExtensions | Allowed extensions without the dot, `null` for any. Ignored for directories.   | No       | `Set<String>?`   | `null`                 |

**Example:**
```kotlin
private val sound by file("Sound", dialogMode = FileDialogMode.OPEN_FILE, supportedExtensions = setOf("ogg"))
```

<hr>

#### `block(name, default)` and `item(name, default)`
Create a setting holding one block or one item, picked from a list in the ClickGUI. <br>

| Property | Description                                | Required | Type               | Default |
|----------|--------------------------------------------|----------|--------------------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String`           |         |
| default  | Initial block or item.                     | Yes      | `Block` or `Item`  |         |

**Example:**
```kotlin
private val ore by block("Ore", Blocks.DIAMOND_ORE)
private val food by item("Food", Items.GOLDEN_APPLE)
```

<hr>

#### `blocks(name, default)`, `items(name, default)` and other registry lists
Create a set of registry entries, picked from a searchable list in the ClickGUI. `default` is a `SequencedSet`, for example `linkedSetOf(...)`. <br>

| Builder        | Entries                                              |
|----------------|------------------------------------------------------|
| `blocks`       | `Block`                                              |
| `items`        | `Item`                                               |
| `sounds`       | `SoundEvent`                                         |
| `mobEffects`   | `MobEffect`                                          |
| `entityTypes`  | `EntityType<*>`                                      |
| `enchantments` | `Identifier` of the enchantment                      |
| `c2sPackets`   | `Identifier` of a packet type sent to the server     |
| `s2cPackets`   | `Identifier` of a packet type received from it       |

**Example:**
```kotlin
private val containers by blocks("Containers", linkedSetOf(Blocks.CHEST, Blocks.BARREL))
private val throwables by items("Throwables", linkedSetOf(Items.ENDER_PEARL, Items.SNOWBALL))
private val alerts by sounds("Alerts", linkedSetOf(SoundEvents.ANVIL_LAND))
private val effects by mobEffects("Effects", linkedSetOf(MobEffects.SPEED.value()))
private val mobs by entityTypes("Mobs", linkedSetOf(EntityTypes.ZOMBIE, EntityTypes.SKELETON))
private val enchantments by enchantments("Enchantments", linkedSetOf(Identifier.withDefaultNamespace("sharpness")))
private val outgoing by c2sPackets("Outgoing", sortedSetOf())
private val incoming by s2cPackets("Incoming", sortedSetOf())
```

A packet matches when `event.packet.type().id in outgoing`.

<hr>

#### `itemList(name, default)`
Creates an ordered list of items, which may contain an item more than once. <br>

| Property | Description                                | Required | Type                | Default |
|----------|--------------------------------------------|----------|---------------------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String`            |         |
| default  | Initial entries.                           | Yes      | `MutableList<Item>` |         |

**Example:**
```kotlin
private val hotbar by itemList("Hotbar", mutableListOf(Items.DIAMOND_SWORD, Items.BOW))
```

<hr>

#### `item(name, default)`
Creates a setting holding a single item. <br>

| Property | Description                                | Required | Type     | Default |
|----------|--------------------------------------------|----------|----------|---------|
| name     | Name under which the setting is displayed. | Yes      | `String` |         |
| default  | Initial value.                             | Yes      | `Item`   |         |

**Example:**
```kotlin
private val weapon by item("Weapon", Items.DIAMOND_SWORD)
```

<hr>

#### `vec2f(name, default)`, `vec3i(name, default, useLocateButton, aliases)` and `vec3d(...)`
Create a vector setting. With `useLocateButton`, the ClickGUI shows a button that sets a 3D vector to the block the player looks at, or to the player's position. <br>

| Property        | Description                                         | Required | Type                           | Default |
|-----------------|-----------------------------------------------------|----------|--------------------------------|---------|
| name            | Name under which the setting is displayed.          | Yes      | `String`                       |         |
| default         | Initial value.                                      | `vec2f` only | `Vector2fc`, `Vec3i` or `Vec3` | zero |
| useLocateButton | Show the locate button (`vec3i`, `vec3d`).          | No       | `Boolean`                      | `true`  |
| aliases         | Former names (`vec3i`, `vec3d`).                    | No       | `List<String>`                 | `[]`    |

**Example:**
```kotlin
private val offset by vec2f("Offset", Vector2f(0f, 0f))
private val home by vec3i("Home", Vec3i.ZERO)
private val anchor by vec3d("Anchor", Vec3.ZERO, useLocateButton = false)
```

<hr>

#### `choices(name, modes)`
Creates a choice between [modes](/docs/add-on-api/developers/creating-modules#modes), each a `Mode` with settings and handlers of its own. Available in modules and other toggleable groups; a `Mode` declares nested modes with `modes(name, active, choices)`. <br>

| Form                                   | Selected by default     |
|----------------------------------------|-------------------------|
| `choices(name, vararg modes)`          | the first mode          |
| `choices(name, active, modes)`         | `active`, from an array |
| `choices(name, activeIndex) { group -> modes }` | the mode at `activeIndex`, from an array the callback builds |

Each mode points back to the group with `override val parent`. `activeMode` returns the selected one.

**Example:**
```kotlin
object ModuleNotifier : ClientModule("Notifier", ModuleCategories.MISC) {

    private val output = choices("Output", Chat, Title)

    private object Chat : Mode("Chat") {
        override val parent get() = output
        val prefix by text("Prefix", "[!]")
    }

    private object Title : Mode("Title") {
        override val parent get() = output
        val duration by int("Duration", 40, 10..200, "ticks")
    }

}
```

<hr>

#### `tree(group)`
Nests a group of settings. A `ValueGroup` only groups them; a `ToggleableValueGroup` also has its own on/off switch, and handlers declared in it only run while it and its parent are enabled. `treeAll(vararg groups)` nests several at once. <br>

| Property | Description             | Required | Type         | Default |
|----------|-------------------------|----------|--------------|---------|
| group    | The group to nest.      | Yes      | `ValueGroup` |         |

**Example:**
```kotlin
object ModuleAutoLog : ClientModule("AutoLog", ModuleCategories.PLAYER) {

    private object Health : ToggleableValueGroup(this, "Health", true) {
        val below by float("Below", 6f, 1f..20f)
    }

    private object Timing : ValueGroup("Timing") {
        val delay by int("Delay", 0, 0..20, "ticks")
    }

    init {
        tree(Health)
        tree(Timing)
    }

}
```

### Modifiers

Every builder returns the `Value`, and these return it again, so they chain:

| Function                     | Effect                                                                                 |
|------------------------------|----------------------------------------------------------------------------------------|
| `visibleWhen { condition }`  | Hides the setting in the ClickGUI while the condition is false. Configs keep it.       |
| `onChange { new -> value }`  | Runs before a new value is applied and returns the value to apply instead.             |
| `onChanged { new -> }`       | Runs after a new value was applied.                                                    |
| `notPersistent()`            | Neither written to nor read from config files. Still shown in the ClickGUI.            |
| `immutable()`                | Keeps the default value.                                                               |
| `doNotIncludeAlways()`       | Left out of configs made for sharing. `doNotIncludeWhen { condition }` does so conditionally. |
| `literalDescription { "..." }` | A fixed description instead of a [translation](/docs/add-on-api/developers/translations).         |

**Example:**
```kotlin
private val mode by enumChoice("Mode", Target.PLAYERS)

private val range by float("Range", 4f, 1f..6f)
    .visibleWhen { mode == Target.MOBS }
    .onChange { it.coerceAtMost(5f) }
    .onChanged { println("Range is now $it") }

private val secret by text("Secret", "")
    .notPersistent()
    .doNotIncludeAlways()
```

`get()`, `set(value)` and `restore()` read, change and reset a `Value` directly. `asStateFlow()` exposes it as a Kotlin `StateFlow`.
