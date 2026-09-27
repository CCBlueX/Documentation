## HUD Components

An add-on can draw components of its own onto the HUD. The [HUD Editor](/docs/theme-system/hud-customization) handles them like a theme's components: it offers them under **Add Component**, the player moves and anchors them, and their settings open next to them.

### Writing a component

A component extends `NativeHudComponent`, reports its size and draws in an `OverlayRenderEvent` handler:

```kotlin
class ClockComponent : NativeHudComponent(
    "Clock",
    enabled = true,
    alignment = Alignment(Alignment.ScreenAxisX.RIGHT, 10, Alignment.ScreenAxisY.TOP, 10),
    description = "Shows the time of day.",
) {

    private val seconds by boolean("Seconds", false)
    private val background by color("Background", Color4b(0, 0, 0, 120))

    override val guiScaledWidth get() = if (seconds) 52f else 36f
    override val guiScaledHeight get() = 13f

    init {
        registerComponentListen(this)
    }

    @Suppress("unused")
    private val renderHandler = handler<OverlayRenderEvent> { event ->
        val bounds = getGuiScaledBounds()
        val pattern = if (seconds) "HH:mm:ss" else "HH:mm"
        val time = Component.literal(LocalTime.now().format(DateTimeFormatter.ofPattern(pattern)))

        event.context.drawQuad(bounds.xMin, bounds.yMin, bounds.xMax, bounds.yMax, background)
        FontManager.FONT_RENDERER.draw(event.context, time, bounds.xMin + 2f, bounds.yMin + 2f)
    }

}
```

A component is a `ToggleableValueGroup` with the HUD module as parent. It has [settings](/docs/add-on-api/settings) like a module, `enabled` is whether it is shown, and its handlers run while it is shown and the HUD module is enabled. See [Rendering](/docs/add-on-api/rendering) for what can be drawn.

#### `NativeHudComponent(name, enabled, alignment, tweaks, description)`
Base class of a component drawn by the client. <br>

| Property    | Description                                                                                  | Required | Type                       | Default |
|-------------|----------------------------------------------------------------------------------------------|----------|----------------------------|---------|
| name        | Name in the HUD Editor and the **Add Component** drawer.                                     | Yes      | `String`                   |         |
| enabled     | Whether the component starts shown.                                                          | Yes      | `Boolean`                  |         |
| alignment   | Default position, see [Alignment](#alignment). The component keeps this instance as its own. | Yes      | `Alignment`                |         |
| tweaks      | Parts of the vanilla HUD to hide while the component is shown, see [Tweaks](#tweaks).        | No       | `Array<HudComponentTweak>` | `[]`    |
| description | Shown in the **Add Component** drawer.                                                       | No       | `String`                   | `""`    |

The default theme's HUD Editor previews its own components by name, `Text` or `Image` for example, so give a component a name no theme component uses.

| Member                               | Description                                                                                                                              |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `guiScaledWidth`, `guiScaledHeight`  | Abstract. The size in GUI-scaled pixels, the HUD Editor draws the component's frame from it.                                             |
| `getGuiScaledBounds(width, height)`  | Protected. Where the component is on screen as a `BoundingBox2f` (`xMin`, `yMin`, `xMax`, `yMax`, `width`, `height`) in GUI-scaled pixels. `width` and `height` default to the component's size. |
| `registerComponentListen(group)`     | Protected. Sends the component to the HUD Editor again whenever a setting in `group` changes. Needed when the size depends on settings. Call it after the settings are declared. |
| `width`, `height`                    | The size in HUD Editor pixels, twice the GUI-scaled size.                                                                                |
| `alignment`                          | The current position.                                                                                                                    |
| `resetAlignment()`                   | Moves the component back to its default position. The HUD Editor does this when the player removes the component.                       |
| `id`                                 | A random `UUID`, new for every instance.                                                                                                 |
| `zIndex`                             | Stacking order in the HUD Editor.                                                                                                        |
| `tweaks`, `componentDescription`     | From the constructor.                                                                                                                    |

### Alignment

`Alignment(horizontalAlignment, horizontalOffset, verticalAlignment, verticalOffset)` anchors a component to an edge or the center of the screen. Horizontal values are `Alignment.ScreenAxisX`, vertical ones `Alignment.ScreenAxisY`.

| Value               | Position of the component                                                   |
|---------------------|-----------------------------------------------------------------------------|
| `LEFT`, `TOP`       | Its left or top edge is `offset` away from the screen's left or top edge.   |
| `RIGHT`, `BOTTOM`   | Its right or bottom edge is `offset` away from the screen's right or bottom edge. |
| `CENTER`            | Its left or top edge is at the screen's center, moved by `offset`.          |
| `CENTER_TRANSLATED` | It is centered on the screen's center, moved by `offset`.                   |

Offsets are `Int`s in HUD Editor pixels, which are GUI-scaled pixels times two, so the clock above sits 5 GUI-scaled pixels from the top right corner. `Alignment.center()` is `Alignment(CENTER, 0, CENTER, 0)`.

The four values are read-only, `setFrom(other)` copies them from another alignment. `alignment.getBounds(width, height)` reads the offsets as screen pixels. A `NativeHudComponent` uses `getGuiScaledBounds()`, which matches the HUD Editor.

### Registering

There are two ways to add a component, both from the add-on's `onInitialize()`.

Registered directly, the component is on the HUD while it is `enabled`. While it is hidden, the **Add Component** drawer lists it under its name and description, and adding it shows it again:

```kotlin
HudComponentManager.register(ClockComponent())
```

Registered through a factory, it is listed in the drawer under the factory's name and description. Every time the player adds it, the factory creates a new component, which is then shown and registered:

```kotlin
HudComponentManager.registerFactory(
    HudComponentFactory.NativeHudComponentFactory(
        "Clock",
        singleton = true,
        description = "Shows the time of day.",
    ) { ClockComponent() }
)
```

#### `NativeHudComponentFactory(name, enabled, singleton, description, function)`
Offers components in the **Add Component** drawer. <br>

| Property    | Description                                                                                  | Required | Type                       | Default |
|-------------|----------------------------------------------------------------------------------------------|----------|----------------------------|---------|
| name        | Name in the drawer. Use the name of the components it creates, `singleton` compares the two. | Yes      | `String`                   |         |
| enabled     | Not read, a component added from the drawer is always shown.                                 | No       | `Boolean`                  | `false` |
| singleton   | Can only be added while no component of that name is shown.                                  | No       | `Boolean`                  | `false` |
| description | Shown in the drawer.                                                                         | No       | `String`                   | `""`    |
| function    | Creates a new component.                                                                     | Yes      | `() -> NativeHudComponent` |         |

### HudComponentManager

#### `register(component)`
Adds a `NativeHudComponent` to the HUD. Registering the same instance again does nothing. <br>

<hr>

#### `unregister(component)`
Takes the component off the HUD Editor and the drawer, and its tweaks stop applying. Its handlers stay registered, so set `enabled = false` first to stop it from drawing. <br>

<hr>

#### `registerFactory(factory)` and `unregisterFactory(factory)`
Adds or removes a factory in the **Add Component** drawer. Components it already created stay. <br>

<hr>

Unlike what an add-on registers through its [own functions](/docs/add-on-api/manifest-and-lifecycle#registering), components and factories are not withdrawn when the add-on fails.

| Member                        | Description                                                                                          |
|-------------------------------|------------------------------------------------------------------------------------------------------|
| `components`                  | Every component, native ones and those of the active theme.                                         |
| `nativeComponents`            | The client's own native components and the registered ones.                                          |
| `getComponent(id)`            | The component whose `id` has that string form, or `null`.                                            |
| `addComponent(id)`            | What the drawer does: creates a component from the factory with that `id`, or shows the hidden component with that `id`. `null` when nothing was added. |
| `isTweakEnabled(tweak)`       | Whether a shown component applies `tweak` while the HUD module is enabled.                           |
| `getComponentWithTweak(tweak)`| The first such component, or `null`.                                                                 |
| `updateComponents()`          | Sends the current components to the HUD Editor.                                                      |

### Saving

The client does not save the components of add-ons. A directly registered component keeps its position and settings across restarts when it is part of one of the add-on's configs:

```kotlin
override fun onInitialize() {
    val clock = ClockComponent()
    HudComponentManager.register(clock)
    config(tree = mutableListOf(clock))
}
```

Components created by a factory are gone after a restart.

### Tweaks

Tweaks apply while the component is shown and the HUD module is enabled.

| Tweak                             | Hides                                                                      |
|-----------------------------------|----------------------------------------------------------------------------|
| `TWEAK_HOTBAR`                    | The vanilla hotbar. Its items are still drawn, placed by the component's alignment. |
| `DISABLE_CROSSHAIR`               | The crosshair.                                                             |
| `DISABLE_SCOREBOARD`              | The scoreboard sidebar.                                                    |
| `DISABLE_STATUS_BAR`              | Health, armor and food.                                                    |
| `DISABLE_EXP_BAR`                 | The experience bar and level.                                              |
| `DISABLE_HELD_ITEM_TOOL_TIP`      | The name of the selected item above the hotbar.                            |
| `DISABLE_OVERLAY_MESSAGE`         | Action bar messages. Messages arriving while it applies are dropped.       |
| `DISABLE_STATUS_EFFECT_OVERLAY`   | The status effect icons.                                                   |
| `DISABLE_LOCATOR_BAR`             | The locator bar.                                                           |
| `DISABLE_SUBTITLE_OVERLAY`        | Vanilla subtitles.                                                         |
