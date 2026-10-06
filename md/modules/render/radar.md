## Radar

Radar draws small directional pointers around the centre of your screen for every rendered entity nearby, giving you a quick heads-up display for awareness without needing to look directly at a target. Each pointer orbits a fixed distance from screen-centre and always points toward the corresponding entity's position relative to you, rotating in sync with your yaw so that "up" on the radar always means "straight ahead."

The **Tilt** setting lets you control whether the radar is shown flat (Static) or dynamically foreshortened based on where you are looking vertically (ByPitch). At 90° the radar looks perfectly flat; lower values compress it vertically, giving a perspective-like feel. ByPitch automatically mirrors your current look pitch, clamped to the range you specify.

You can customise the look of each pointer — choose between a sharp triangle shape with tunable dimensions or one of two pre-built image styles — and colour them by entity distance, health, a fixed colour, or a cycling rainbow. The **Alpha** curve lets you fade pointers out smoothly as entities get further away. Enable **OnlyPlayers** to ignore mobs and only track other players, which is useful on PvP servers where mob noise would otherwise clutter the display. Radar pairs well with [ESP](/docs/modules/render/esp) and [Nametags](/docs/modules/render/nametags) for a complete awareness setup.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Tilt | Mode Selector | Static | — | Controls how the radar is tilted. Static applies a fixed angle; ByPitch dynamically tilts based on your look pitch. |
| Tilt → Static → Angle | Decimal | 90.0 | -90.0 – 90.0 deg | Fixed tilt angle applied to the radar. 90° renders it flat; lower values compress it vertically. |
| Tilt → ByPitch → Limitation | Decimal Range | 45.0..90.0 | 0.0 – 90.0 deg | The pitch range (in degrees) that is allowed to influence the radar tilt. Values outside this range are clamped. |
| Radius | Decimal | 40.0 | 2.0 – 200.0 | Distance in pixels from the screen centre at which pointers are drawn. |
| OnlyPlayers | Toggle | false | — | When on, only player entities appear on the radar; mobs and other entities are ignored. |
| PointerMode | Mode Selector | Triangle | — | Shape used to represent each entity on the radar. |
| PointerMode → Triangle → Width | Decimal | 8.0 | 1.0 – 100.0 | Horizontal width of the triangle pointer. |
| PointerMode → Triangle → Height | Decimal | 10.0 | 1.0 – 100.0 | Vertical height of the triangle pointer. |
| PointerMode → Triangle → TailConcaveSize | Decimal | 2.0 | 0.0 – 50.0 | How far the base of the triangle is notched inward. Set to 0 for a plain triangle. |
| PointerMode → Image1 → Size | Decimal | 10.0 | 1.0 – 100.0 | Display size of the Image1 pointer texture. |
| PointerMode → Image2 → Size | Decimal | 10.0 | 1.0 – 100.0 | Display size of the Image2 pointer texture. |
| ColorMode | Mode Selector | Health | — | Determines how pointer colours are assigned to entities. |
| ColorMode → Distance → Saturation | Decimal | 1.0 | 0.0 – 1.0 | Colour saturation used when colouring by distance. |
| ColorMode → Distance → Brightness | Decimal | 1.0 | 0.0 – 1.0 | Colour brightness used when colouring by distance. |
| ColorMode → Distance → Hue | Curve | — | — | Curve mapping entity distance to a hue value when colouring by distance. |
| ColorMode → Health → Alpha | Integer | 255 | 0 – 255 | Opacity of pointers when colouring by entity health. |
| ColorMode → Static → Color | Color | — | — | Fixed colour applied to all pointers in Static colour mode. |
| Alpha | Curve | — | — | Curve mapping entity distance to pointer opacity, allowing far-away entities to fade out gradually. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleRadar.kt)*
