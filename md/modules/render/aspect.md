## Aspect

Aspect lets you stretch or squash your game view horizontally without touching your in-game FOV. Lowering the ratio narrows everything into a tall, pinched look, while raising it widens the world so it spills out toward the edges of your screen — a quick way to get a fisheye or stretched effect for visibility or just for style.

By default the ratio sits at 100%, which is the normal, untouched view. Drag it below 100% to compress the picture inward, or above 100% to stretch it wider. The change applies the moment the module is enabled, so you can dial in the exact amount of distortion you want and see it instantly.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Ratio | Integer | 100 | 1..300 (%) | How much the view is stretched horizontally. 100% is normal; lower values pinch the view inward and higher values widen it. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleAspect.kt)*
