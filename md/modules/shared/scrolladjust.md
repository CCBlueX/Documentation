## ScrollAdjust

ScrollAdjust lets you fine-tune a value on the fly by scrolling your mouse wheel instead of opening a menu and typing a number. While the module that uses it is active, scrolling up or down nudges the value smoothly in real time, so you can dial in exactly what you want while playing.

To avoid scrolling the value by accident, you can require a modifier key to be held down before scrolling counts — for example, holding the key and scrolling adjusts the value, while scrolling on its own keeps working normally (such as switching hotbar slots). If no modifier key is set, scrolling always adjusts the value. The Sensitivity option controls how much each scroll tick changes the value: lower values give slower, more precise adjustments, while higher values move it faster.

In [CameraClip](/docs/modules/render/cameraclip) this controls the third-person camera distance, and in [AirPlace](/docs/modules/world/airplace) it adjusts that module's targeted value — but the behavior is the same everywhere: hold the modifier (if set) and scroll to change the value.

This setting group is used by the following modules:
- [AirPlace](/docs/modules/world/airplace)
- [CameraClip](/docs/modules/render/cameraclip)

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Modifier | Key | — | — | The key you must hold for scrolling to adjust the value. Leave unbound to always adjust on scroll. |
| Sensitivity | Decimal | 0.5 | 0.1..1.0 | How much each scroll tick changes the value. Lower is slower and more precise; higher moves faster. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/cameraclip/ScrollAdjustValueGroup.kt)*
