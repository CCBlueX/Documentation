## BlockOutline

BlockOutline replaces the thin black box around the block you look at with a colored one. It helps when the normal outline is hard to see.

With SideOnly on, only the side you look at is colored. With Slide on, the box glides to the next block when you look around (not for blocks with odd shapes like stairs).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| SideOnly | Toggle | true | | Colors only the side you look at. Off colors the whole block. |
| Color | Color | Light blue, see-through | | Fill color. |
| Outline | Color | Light blue | | Border color. |
| Slide | Toggleable Group | On | | Moves the box smoothly from block to block. |
| Slide → Time | Integer | 150 ms | 1..1000 ms | How long the move takes. |
| Slide → Easing | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the movement speeds up and slows down. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBlockOutline.kt)*
