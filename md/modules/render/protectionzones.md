## ProtectionZones

Allows you to see areas protected by protection blocks and suggests optimal placement spots.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── ProtectionBlocks (Registry List)
├── ProtectionRadius (Setting Group)
│   ├── RadiusX (Integer | default: 20 | range: 1..256 | blocks)
│   ├── RadiusZ (Integer | default: 20 | range: 1..256 | blocks)
│   └── RadiusY (Integer | default: 383 | range: 1..383 | blocks)
├── PlacementIndicator (Setting Group)
│   └── SnapToY (Toggle | default: false)
└── Renderer (Setting Group)
    ├── RenderLimit (Integer | default: 16 | range: 3..50 | zones)
    ├── HoldBlockToRender (Toggle | default: false)
    ├── ProtectionColors (Setting Group)
    │   ├── ZoneFill (Color)
    │   ├── ZoneOutline (Color)
    │   └── CenterZoneOutline (Color)
    └── IndicatorColors (Setting Group)
        ├── IndicatorOutline (Color)
        └── IndicatorFill (Color)
```

### Settings Details

- **ProtectionBlocks** (Registry List) — Defines which blocks are considered protection blocks.
#### ProtectionRadius

A group of related settings.

- **RadiusX** (Integer) — default: `20`; range: `1` – `256`; unit: blocks — Sets the protection zone radius on the X axis.
- **RadiusZ** (Integer) — default: `20`; range: `1` – `256`; unit: blocks — Sets the protection zone radius on the Z axis.
- **RadiusY** (Integer) — default: `383`; range: `1` – `383`; unit: blocks — Sets the protection zone radius on the Y axis.

#### PlacementIndicator

A group of related settings.

- **SnapToY** (Toggle) — default: `false` — Snaps the placement indicator Y position to the reference protection block.

#### Renderer

A group of related settings.

- **RenderLimit** (Integer) — default: `16`; range: `3` – `50`; unit: zones — Limits the maximum number of zones rendered at once.
- **HoldBlockToRender** (Toggle) — default: `false` — Only renders zones when holding a protection block.
##### ProtectionColors

A group of related settings.

- **ZoneFill** (Color) — Sets the fill color for highlighted protection zones.
- **ZoneOutline** (Color) — Sets the outline color for protection zone boundaries.
- **CenterZoneOutline** (Color) — Sets the outline color for protection block center markers.

##### IndicatorColors

A group of related settings.

- **IndicatorOutline** (Color) — Sets the outline color for the placement indicator.
- **IndicatorFill** (Color) — Sets the fill color for the placement indicator.



### Screenshots

*Screenshots for ProtectionZones will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleProtectionZones.kt)*
