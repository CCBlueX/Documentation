## Zoom

Zoom lets you narrow your field of view on demand, making distant objects appear larger and easier to see — useful for scouting terrain, reading signs, or tracking players at range. The module is bound to a **hold** action by default, meaning zoom is active only while you keep the key held down and releases as soon as you let go.

When you enable Zoom, the view smoothly transitions from your normal FOV to the zoomed-in level using the easing curve and duration you configure. The same smooth transition plays in reverse when you release the key. If **Scroll** is enabled, you can adjust the zoom level on the fly by scrolling your mouse wheel while zoomed in, letting you fine-tune magnification without opening the settings.

This module interacts with [NoFOV](/docs/modules/render/nofov) — if that module is active, Zoom uses its modified FOV as the baseline rather than your vanilla FOV setting.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Zoom | Integer | 30 | 10–150 | The target field-of-view (in degrees) when zoomed in. Lower values mean greater magnification. |
| Scroll | Toggleable Group | on | — | When enabled, scrolling the mouse wheel while zoomed adjusts the zoom level in real time. |
| Scroll → Speed | Decimal | 2.0 | 0.5–8.0 | How many FOV degrees each scroll tick shifts the zoom level. Higher values make the scroll wheel change zoom more aggressively. |
| Transition | Choice | QuadIn | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | Easing curve applied to the zoom-in and zoom-out animation. |
| DurationFactor | Decimal | 2.0 | 0.0–10.0 | Scales how long the transition animation takes. Higher values produce a slower, more gradual zoom; 0.0 makes it instant. Unit: x |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleZoom.kt)*
