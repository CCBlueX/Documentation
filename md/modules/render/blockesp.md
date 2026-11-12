## BlockESP

BlockESP shows chosen blocks through walls, so you can find them from far away. By default it looks for beds and dragon eggs, which helps in Bed Wars. For ores, [XRay](/docs/modules/render/xray) works better, and for chests use [StorageESP](/docs/modules/render/storageesp).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Box | Box, Glow | Box draws a see-through box, Glow makes the block glow. |
| Mode → [Glow] → Style | Mode Selector | Smooth | Vanilla, Smooth, Outline, Neon, Rainbow, Ripple, Hologram, Halftone, Chromatic, Aura | How the glow looks. The styles and their settings are the same as in [ESP](/docs/modules/render/esp). |
| Mode → [Box] → Outline | Toggle | true | | Adds a border around each box. |
| Targets | Registry List | All beds, Dragon Egg | | The blocks to show. |
| ColorMode | Mode Selector | MapColor | MapColor, Static, Rainbow | MapColor uses the block's own color, Static one color, Rainbow changing colors. |
| ColorMode → [Static] → Color | Color | Orange | | The color for Static. |
| DistanceFade | Setting Group | | | See [Shared: DistanceFade](/docs/modules/shared-settings/distancefade). |
| MergeAdjacent | Toggle | false | | Joins blocks that touch into one shape. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBlockESP.kt)*
