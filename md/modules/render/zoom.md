## Zoom

Zoom lets you see far away things bigger while you hold its key. Let go and your view goes back to normal. With **Scroll** on, the mouse wheel changes how far you zoom.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Zoom | Integer | 30 | 10 to 150 | Field of view while zoomed, in degrees. Lower values zoom in more. |
| Scroll | Toggleable Group | on | | Lets you change the zoom with the mouse wheel while zoomed. |
| Scroll → Speed | Decimal | 2.0 | 0.5 to 8.0 | How much each scroll step changes the zoom. |
| Transition | Choice | QuadIn | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the zoom speeds up or slows down when it starts and ends. |
| DurationFactor | Decimal | 2.0 | 0.0 to 10.0 x | How long zooming in and out takes. Higher is slower, 0 is instant. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleZoom.kt)*
