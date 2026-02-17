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
├── Mode (Mode Selector | default: Glow | modes: Glow, Box)
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

Select a mode for this feature. Available modes: **Glow**, **Box**. Default: **Glow**.

#### ColorMode

Select a mode for this feature. Available modes: **Static**, **Rainbow**. Default: **Static**.

##### Mode: Static

- **Color** (Color) — Static color applied to all highlighted items.

### Screenshots

*Screenshots for ItemESP will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleItemESP.kt)*
