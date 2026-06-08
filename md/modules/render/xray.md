## XRay

XRay hides every block in the world except the ones on your allow-list, letting you see ores, chests, and other valuable blocks straight through solid terrain. It is one of the most effective tools for locating resources quickly, especially when caving or strip-mining in the deep-slate layer where diamond and ancient debris are found.

By default, the block list already includes all overworld and Nether ores (including their deepslate variants), every storage block (chests, shulker boxes, hoppers, etc.), liquids, portals, and a range of utility blocks. You can customise this list at any time using the in-game `/xray` command — add or remove individual blocks to tune exactly what gets shown. Enabling [FullBright](/docs/modules/render/fullbright) behaviour is built in so your targets are always clearly lit, and the optional **ExposedOnly** filter narrows the view further to blocks that have at least one non-solid neighbour, cutting down visual noise in densely packed ore clusters.

If you want highlights rather than hiding everything else, consider pairing XRay with [BlockESP](/docs/modules/render/blockesp), which draws outlines around specific blocks without affecting normal world rendering.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| FullBright | Toggle | true | — | Renders all visible blocks at full brightness so highlighted targets are never obscured by darkness. |
| ExposedOnly | Toggle | false | — | When enabled, only shows blocks that are exposed to at least one non-solid neighbouring block, reducing clutter from fully buried blocks. |
| Blocks | Registry List | — | — | The list of blocks that XRay will render. All other blocks are hidden. Pre-populated with ores, storage blocks, liquids, portals, and other notable blocks; fully customisable. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleXRay.kt)*
