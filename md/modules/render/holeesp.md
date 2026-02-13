## HoleESP

Detects and displays safe spots for crystal PvP.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: GlowingPlane | modes: Box, GlowingPlane)
│   ├── [Mode: Box]
│   │   └── Outline (Toggle | default: true)
│   └── [Mode: GlowingPlane]
│       ├── Outline (Toggle | default: true)
│       └── GlowHeight (Decimal | default: 0.7 | range: 0.0..1.0)
├── HorizontalScanDistance (Integer | default: 32 | range: 4..128)
├── VerticalScanDistance (Integer | default: 8 | range: 4..128)
├── DistanceFade (Decimal | default: 0.3 | range: 0.0..1.0)
├── 1x1Bedrock (Color)
├── 1x1 (Color)
├── 1x2 (Color)
└── 2x2 (Color)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Box**, **GlowingPlane**. Default: **GlowingPlane**.

##### Mode: Box

- **Outline** (Toggle) — default: `true` — Draws an outline around hole boxes.

##### Mode: GlowingPlane

- **Outline** (Toggle) — default: `true` — Draws an outline on the bottom plane.
- **GlowHeight** (Decimal) — default: `0.7`; range: `0.0` – `1.0` — Height of the upward glow effect from the base.

- **HorizontalScanDistance** (Integer) — default: `32`; range: `4` – `128` — Horizontal range in blocks to scan for holes.
- **VerticalScanDistance** (Integer) — default: `8`; range: `4` – `128` — Vertical range in blocks to scan for holes.
- **DistanceFade** (Decimal) — default: `0.3`; range: `0.0` – `1.0` — Fades hole colors based on distance from the player.
- **1x1Bedrock** (Color) — Color for 1×1 holes made entirely of bedrock.
- **1x1** (Color) — Color for standard 1×1 holes.
- **1x2** (Color) — Color for 1×2 holes.
- **2x2** (Color) — Color for 2×2 holes.

### Screenshots

*Screenshots for HoleESP will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleHoleESP.kt)*
