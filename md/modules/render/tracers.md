## Tracers

Tracers draws a line from the center of your screen to every nearby entity within a set range, giving you an at-a-glance map of where targets are even when they are off to the side, behind terrain, or obscured by other players. The lines update smoothly in real time as entities move, and only appear for targets within your configured maximum distance, so the display stays focused on what is actually relevant to you.

You can choose from four color modes to make the lines as readable as possible. **Distance** shifts the hue along a configurable curve based on how far away a target is. **Health** tints lines to reflect each entity's remaining health. **Static** uses a single fixed color for everything. **Rainbow** cycles through colors automatically. Regardless of which mode is active, any player you have added as a friend is always highlighted in blue. Tracers pairs well with [ESP](/docs/modules/render/esp) and [Nametags](/docs/modules/render/nametags) for comprehensive visual awareness during combat.

Increase **LineWidth** to make tracers pop in cluttered scenes, or lower **MaximumDistance** to reduce visual noise and focus only on close-range threats.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ColorMode | Mode Selector | Distance | — | Determines how tracer lines are colored. Modes: Distance, Health, Static, Rainbow. |
| ColorMode → Distance → Saturation | Decimal | 1.0 | 0.0–1.0 | Color saturation of the HSB gradient in Distance mode. |
| ColorMode → Distance → Brightness | Decimal | 1.0 | 0.0–1.0 | Color brightness of the HSB gradient in Distance mode. |
| ColorMode → Distance → Hue | Curve | — | — | Curve controlling how hue shifts as target distance increases. |
| ColorMode → Distance → Alpha | Decimal | 1.0 | 0.0–1.0 | Opacity of tracer lines in Distance mode. |
| ColorMode → Health → Alpha | Integer | 255 | 0–255 | Opacity of tracer lines in Health mode. |
| ColorMode → Static → Color | Color | — | — | Fixed color applied to all tracer lines in Static mode. |
| LineWidth | Decimal | 1.0 | 1.0–16.0 | Thickness of the tracer lines in pixels. |
| MaximumDistance | Decimal | 128.0 | 1.0–512.0 | Maximum distance in blocks at which tracer lines are drawn to entities. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleTracers.kt)*
