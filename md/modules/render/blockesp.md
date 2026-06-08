## BlockESP

BlockESP highlights specific block types through walls, so you can spot them from a distance no matter what's in the way. It works by scanning loaded chunks for the blocks you choose in **Targets** and drawing them with a visible overlay. Out of the box it's tuned to find beds and dragon eggs, which makes it handy for Bed Wars and similar modes where locating enemy beds quickly matters.

Pick how the highlight looks with **Mode** — a filled box, a soft glow, or a clean outline — and control the coloring with **ColorMode**, ranging from each block's natural map color to a single static color or an animated rainbow. **DistanceFade** softens the rendering for blocks that are far away so nearby targets stand out more, and **MergeAdjacent** combines touching blocks into one shape for a cleaner look when targets are clustered together.

If you specifically want to see ores through terrain, [XRay](/docs/modules/render/xray) is the more focused tool, while [StorageESP](/docs/modules/render/storageesp) is better suited to chests and other containers.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Outline | Box, Glow, Outline | How target blocks are drawn: a filled Box, a soft Glow, or a crisp Outline. |
| Mode → Box → Outline | Toggle | true | — | Adds an outline around the filled boxes in Box mode. |
| Targets | Registry List | — | — | The list of block types to highlight. |
| ColorMode | Mode Selector | MapColor | MapColor, Static, Rainbow | How highlights are colored: each block's natural map color, one fixed color, or a shifting rainbow. |
| ColorMode → Static → Color | Color | — | — | The fixed color used when ColorMode is set to Static. |
| DistanceFade | Setting Group | — | — | See [Shared: DistanceFade](/docs/modules/shared-settings/distancefade). |
| MergeAdjacent | Toggle | false | — | Merges touching target blocks of the same type into a single shape for a cleaner overlay. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBlockESP.kt)*
