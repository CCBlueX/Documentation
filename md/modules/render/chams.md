## Chams

Chams (short for "chameleon") makes players render through walls by drawing them with a special set of render pipelines that defeat the normal depth test. Instead of being hidden behind terrain, entities show up as solid, always-visible silhouettes, so you can track opponents even when they duck behind blocks, hide in buildings, or stand in caves.

It's a Render-category visual aid you'd typically pair with combat or tracking: when Chams is on, you keep a constant read on where players are without relying on line of sight. Under the hood it swaps in custom render types whose [depth-stencil state always passes the depth test](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleChams.kt#L43-L47), which is what lets the model draw on top of geometry that would otherwise occlude it. It provides [translucent, cutout, and no-cull pipelines](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleChams.kt#L49-L116) so different parts of the model render correctly.

Chams offers two **Mode**s. **Normal** draws the classic always-visible silhouette described above. **Image** instead fills each visible entity with an image of your choice, so it reads like a textured cutout of the player. The image can be tiled, stretched, or scaled to cover the screen, filtered, and shifted with an offset. Note that there is a known issue with how player armor and held items are rendered while Chams is active.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Normal | — | How visible entities are drawn: a plain silhouette or an image fill. |
| Mode → [Image] → File | File | — | — | The PNG or JPG image drawn over entities. |
| Mode → [Image] → Mapping | Mode Selector | Repeat | — | How the image is fitted to the screen: **Repeat** tiles it, **Stretch** scales it to the screen, **Cover** scales it to fill while keeping its aspect ratio. |
| Mode → [Image] → Mapping → [Repeat] → TileWidth | Integer | 256 | 16..2048 px | Width of each repeated tile. |
| Mode → [Image] → Filtering | Choice | Nearest | — | Texture filtering applied to the image: Nearest or Linear. |
| Mode → [Image] → Offset | Vector2_f | 0, 0 | — | Shifts the image horizontally and vertically. |

---
*Last updated: 2026-07-29 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleChams.kt)*
