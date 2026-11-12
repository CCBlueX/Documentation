## Tracers

Tracers draws a line from the middle of your screen to every entity near you, so you can see where they are even behind blocks. Friends always get a blue line.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ColorMode | Mode Selector | Distance | Distance, Health, Static, Rainbow | How the lines are colored. |
| ColorMode → Distance → Saturation | Decimal | 1.0 | 0.0 to 1.0 | How strong the colors are. |
| ColorMode → Distance → Brightness | Decimal | 1.0 | 0.0 to 1.0 | How bright the colors are. |
| ColorMode → Distance → Hue | Curve | | Distance 0 to 200, Hue 0 to 360 | Which color a line gets at each distance. |
| ColorMode → Distance → Alpha | Decimal | 1.0 | 0.0 to 1.0 | How see-through the lines are. |
| ColorMode → Health → Alpha | Integer | 255 | 0 to 255 | How see-through the lines are when colored by health. |
| ColorMode → Static → Color | Color | | | One color for every line. |
| LineWidth | Decimal | 1.0 | 1.0 to 16.0 | How thick the lines are. |
| MaximumDistance | Decimal | 128.0 | 1.0 to 512.0 | Entities farther away than this get no line. |
| Render | Choice | Plain | Plain, Shader | **Plain** draws the lines normally. **Shader** draws them with a shader effect, and its **Style** setting picks how that looks. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleTracers.kt)*
