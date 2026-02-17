## TNTTimer

Highlight the active TNTs.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── ESP (Toggle | default: true)
└── ShowTimer (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── Scale (Decimal | default: 1.5 | range: 0.25..4.0)
    ├── RenderY (Decimal | default: 1.0 | range: -2.0..2.0)
    ├── OwnerName (Toggle | default: true)
    └── TimeUnit (Choice | default: TICKS | options: Ticks, Seconds)
```

### Settings Details

- **ESP** (Toggle) — default: `true` — Enables glow ESP highlighting on active TNT entities.
#### ShowTimer

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Enables the on-screen timer display for TNT.
- **Scale** (Decimal) — default: `1.5`; range: `0.25` – `4.0` — Sets the text scale of the timer display.
- **RenderY** (Decimal) — default: `1.0`; range: `-2.0` – `2.0` — Adjusts the vertical offset of the timer display.
- **OwnerName** (Toggle) — default: `true` — Shows the name of the player who placed the TNT.
- **TimeUnit** (Choice) — default: `TICKS`; options: `Ticks`, `Seconds` — Selects the time unit for the fuse countdown display.


### Screenshots

*Screenshots for TNTTimer will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleTNTTimer.kt)*
