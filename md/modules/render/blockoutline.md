## BlockOutline

BlockOutline replaces Minecraft's default thin black block highlight with a fully customizable outline and a colored face overlay. Point at any block and instead of the vanilla wireframe you get a filled box (or just the face you're looking at) drawn in colors you choose, so the block you're about to break or place against stands out clearly.

Use it whenever the stock highlight is too faint to read — bright environments, fast PvP, or detailed builds where you want to be sure exactly which block and which side is targeted. The module reads your current crosshair target each frame, builds the block's collision shape, and draws a fill plus an outline over it. For blocks with a simple single-box shape it can also animate the highlight, sliding smoothly from the old block to the new one as you move your aim; complex shapes (stairs, fences, etc.) are drawn directly without the slide. See [the render handler](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBlockOutline.kt#L72-L153) for how the target shape and animation are resolved.

When **SideOnly** is on, only the face you're looking at is highlighted (the box is flattened to that side via [`flatBox`](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBlockOutline.kt#L155-L162)); with it off, the whole block box is drawn.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| SideOnly | Toggle | true | — | When on, highlights only the face you are aiming at; when off, draws the full block box. |
| Color | Color | Color4b(68, 117, 255, 70) | — | Fill color of the highlighted face or box (the default is a semi-transparent blue). |
| Outline | Color | Color4b(68, 117, 255, 150) | — | Color of the outline drawn around the highlighted shape. |
| Slide | Toggleable Group | on | — | When enabled, animates the highlight sliding from the previous block to the newly targeted one (single-box shapes only). |
| Slide → Time | Integer | 150 | 1..1000 (ms) | Duration of the slide animation in milliseconds. |
| Slide → Easing | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | Easing curve used to interpolate the slide between blocks. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBlockOutline.kt)*
