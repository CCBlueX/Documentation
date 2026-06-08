## Chams

Chams (short for "chameleon") makes players render through walls by drawing them with a special set of render pipelines that defeat the normal depth test. Instead of being hidden behind terrain, entities show up as solid, always-visible silhouettes, so you can track opponents even when they duck behind blocks, hide in buildings, or stand in caves.

It's a Render-category visual aid you'd typically pair with combat or tracking: when Chams is on, you keep a constant read on where players are without relying on line of sight. Under the hood it swaps in custom render types whose [depth-stencil state always passes the depth test](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleChams.kt#L43-L47), which is what lets the model draw on top of geometry that would otherwise occlude it. It provides [translucent, cutout, and no-cull pipelines](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleChams.kt#L49-L116) so different parts of the model render correctly.

This module has no configurable settings — toggle it on and off. Note that there is a known issue with how player armor and held items are rendered while Chams is active.

**Category:** Render
**Enabled by default:** No

### Settings

This module has no configurable settings.

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleChams.kt)*
