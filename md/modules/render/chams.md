## Chams

Chams shows players through walls, so you can see where they are even behind blocks.

In Normal mode, players are drawn on top of everything. Image mode fills them with a picture you choose. Armor and held items can look wrong while Chams is on.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Normal | Normal, Image | Normal shows players through walls, Image fills them with a picture. |
| Mode → [Image] → File | File | | | The PNG or JPG picture to use. |
| Mode → [Image] → Mapping | Mode Selector | Repeat | Repeat, Stretch, Cover | Repeat tiles the picture, Stretch stretches it over the screen, Cover fills the screen and keeps its shape. |
| Mode → [Image] → Mapping → [Repeat] → TileWidth | Integer | 256 px | 16..2048 px | Width of each tile. |
| Mode → [Image] → Filtering | Choice | Nearest | Nearest, Linear | Nearest keeps pixels sharp, Linear makes them smooth. |
| Mode → [Image] → Offset | Vector2_f | 0, 0 | | Moves the picture sideways and up or down. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleChams.kt)*
