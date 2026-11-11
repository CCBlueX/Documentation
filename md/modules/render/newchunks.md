## NewChunks

NewChunks colors chunks the server has just created for the first time differently from old chunks. It spots new chunks by water or lava that is still flowing. Use it on anarchy or big survival servers to find land where nobody has been yet.

The colors are drawn as a flat layer at a height you choose. With **Persist** on, chunks keep their color after they unload, so your map grows while you play.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| RenderDistance | Integer | 32 | 4 to 128 chunks | How far away chunks are colored. |
| RenderY | Decimal | 0.0 | -64.0 to 320.0 | The height of the colored layer. Not used when AutoY is on. |
| AutoY | Toggle | false | | Puts the layer 100 blocks below you. |
| Smooth | Toggle | true | | Blends the colors of old chunks next to new ones, so the border is softer. |
| Persist | Toggle | true | | Remembers chunks after they unload. |
| NewColor | Color | 0, 255, 0, 80 | | Color of new chunks. |
| OldColor | Color | 255, 0, 0, 80 | | Color of old chunks. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleNewChunks.kt)*
