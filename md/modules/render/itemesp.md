## ItemESP

ItemESP highlights items on the ground, so you can see them through walls and from far away. It can also highlight arrows and tridents you can pick up.

Use **Filter** and **Items** to choose which items show. With **Blacklist** every item shows except the ones in the list. With **Whitelist** only the ones in the list show. Turn on **Tracers** to draw a line from you to each item, like the [Tracers](/docs/modules/render/tracers) module.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Filter | Choice | Blacklist | Whitelist, Blacklist | Whether the Items list picks the items to show or the items to hide. |
| Items | Registry List | Empty | | The items used by Filter. |
| MaximumDistance | Decimal | 128.0 | 1.0 to 512.0 | How far away items are still highlighted, in blocks. |
| Tracers | Toggle | false | | Draws a line from you to each highlighted item. |
| ShowArrows | Toggleable Group | On | | Highlights arrows you can pick up. |
| ShowArrows → RegularArrows | Toggle | true | | Normal arrows. |
| ShowArrows → SpectralArrows | Toggle | true | | Spectral arrows. |
| ShowArrows → ArrowsWithEffects | Toggle | true | | Tipped arrows with potion effects. |
| ShowTridents | Toggle | true | | Highlights thrown tridents. |
| Mode | Mode Selector | Glow | Glow, Box, Legacy2D | How items are highlighted: a glow, a 3D box, or a flat marker. |
| Mode → Box → MergeIntersecting | Toggle | false | | Joins boxes that overlap into one shape. |
| Mode → Legacy2D → Scale | Decimal | 0.1 | 0.02 to 0.3 | Size of the marker. |
| Mode → Legacy2D → YOffset | Decimal | 0.0 | -1.0 to 1.0 | Moves the marker up or down. |
| Mode → Legacy2D → BackgroundAlpha | Integer | 150 | 0 to 255 | How see-through the marker's background is. |
| ColorMode | Mode Selector | Static | Static, Rainbow | How the highlight is colored. |
| ColorMode → Static → Color | Color | 255, 179, 72, 255 | | The highlight color. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleItemESP.kt)*
