## BlockESP

Allows you to see selected blocks through walls.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Box | modes: Box, Glow, Outline)
│   ├── [Mode: Box]
│   │   └── Outline (Toggle | default: true)
├── Targets (Registry List)
├── ColorMode (Mode Selector | default: MapColor | modes: MapColor, Static, Rainbow)
│   ├── [Mode: Static]
│   │   └── Color (Color)
├── DistanceFade (Setting Group)
│   ├── NearStart (Decimal | default: 0.0 | range: 0.0..512.0)
│   ├── NearEnd (Decimal | default: 0.0 | range: 0.0..512.0)
│   ├── FarStart (Decimal | default: 512.0 | range: 0.0..512.0)
│   └── FarEnd (Decimal | default: 512.0 | range: 0.0..512.0)
└── MergeAdjacent (Toggle | default: false)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Box**, **Glow**, **Outline**. Default: **Box**.

##### Mode: Box

- **Outline** (Toggle) — default: `true` — Draws an outline that follows the real shape of each highlighted block.

- **Targets** (Registry List) — Blocks to highlight through walls.
#### ColorMode

Select a mode for this feature. Available modes: **MapColor**, **Static**, **Rainbow**. Default: **MapColor**.

##### Mode: Static

- **Color** (Color) — Static color applied to all highlighted blocks.

#### DistanceFade

> *This is a shared settings group defined in `DistanceFadeUniformValueGroup`. See also: other modules using distance-based fading.*

A group of related settings.

- **NearStart** (Decimal) — default: `0.0`; range: `0.0` – `512.0`
- **NearEnd** (Decimal) — default: `0.0`; range: `0.0` – `512.0`
- **FarStart** (Decimal) — default: `512.0`; range: `0.0` – `512.0`
- **FarEnd** (Decimal) — default: `512.0`; range: `0.0` – `512.0`

- **MergeAdjacent** (Toggle) — default: `false` — Merges touching blocks into a single combined shape instead of outlining each block separately.

### Screenshots

*Screenshots for BlockESP will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleBlockESP.kt)*
