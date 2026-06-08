## ItemESP

Allows you to see dropped items through walls.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Filter (Choice | default: BLACKLIST | options: Whitelist, Blacklist)
├── Items (Registry List)
├── MaximumDistance (Decimal | default: 128.0 | range: 1.0..512.0)
├── Tracers (Toggle | default: false)
├── ShowArrows (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── RegularArrows (Toggle | default: true)
│   ├── SpectralArrows (Toggle | default: true)
│   └── ArrowsWithEffects (Toggle | default: true)
├── ShowTridents (Toggle | default: true)
├── Mode (Mode Selector | default: Glow | modes: Glow, Box, Legacy2D)
│   ├── [Mode: Box]
│   │   └── MergeIntersecting (Toggle | default: false)
│   └── [Mode: Legacy2D]
│       ├── Scale (Decimal | default: 0.1 | range: 0.02..0.3)
│       ├── YOffset (Decimal | default: 0.0 | range: -1.0..1.0)
│       └── BackgroundAlpha (Integer | default: 150 | range: 0..255)
└── ColorMode (Mode Selector | default: Static | modes: Static, Rainbow)
    ├── [Mode: Static]
    │   └── Color (Color)
```

### Settings Details

- **Filter** (Choice) — default: `BLACKLIST`; options: `Whitelist`, `Blacklist` — Whether the item list acts as a whitelist or blacklist.
- **Items** (Registry List) — List of items to include or exclude.
- **MaximumDistance** (Decimal) — default: `128.0`; range: `1.0` – `512.0` — Maximum render distance for highlighted items.
- **Tracers** (Toggle) — default: `false` — Draws lines from your view to dropped items.
#### ShowArrows

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles rendering of collectible arrows.
- **RegularArrows** (Toggle) — default: `true` — Shows regular arrows on the ground.
- **SpectralArrows** (Toggle) — default: `true` — Shows spectral arrows on the ground.
- **ArrowsWithEffects** (Toggle) — default: `true` — Shows tipped arrows on the ground.

- **ShowTridents** (Toggle) — default: `true` — Shows thrown tridents on the ground.
#### Mode

Select a mode for this feature. Available modes: **Glow**, **Box**, **Legacy2D**. Default: **Glow**.

##### Mode: Box

- **MergeIntersecting** (Toggle) — default: `false` — Merges overlapping item boxes into a single outline.

##### Mode: Legacy2D

Classic flat box rendered around the item (the old 2D style).

- **Scale** (Decimal) — default: `0.1`; range: `0.02` – `0.3` — Size of the legacy box.
- **YOffset** (Decimal) — default: `0.0`; range: `-1.0` – `1.0` — Vertical offset of the legacy box.
- **BackgroundAlpha** (Integer) — default: `150`; range: `0` – `255` — Opacity of the box background fill.

#### ColorMode

Select a mode for this feature. Available modes: **Static**, **Rainbow**. Default: **Static**.

##### Mode: Static

- **Color** (Color) — Static color applied to all highlighted items.

### Screenshots

*Screenshots for ItemESP will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleItemESP.kt)*
