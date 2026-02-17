## Eagle

Automatically sneaks at the edge of a block

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── EdgeDistance (Decimal Range | default: 0.4..0.6 | range: 0.01..1.3)
└── Conditional (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── Conditions (Multi-Select | default: [OnGround] | options: Left, Right, Forwards, Backwards, HoldingBlocks, OnGround, Sneak)
    └── Pitch (Decimal Range | default: -90.0..90.0 | range: -90.0..90.0)
```

### Settings Details

- **EdgeDistance** (Decimal Range) — default: `0.4` – `0.6`; range: `0.01` – `1.3` — How close to the block edge you must be before sneaking activates.
#### Conditional

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Conditions** (Multi-Select) — default: `OnGround`; options: `Left`, `Right`, `Forwards`, `Backwards`, `HoldingBlocks`, `OnGround`, `Sneak` — Required conditions for Eagle to activate.
- **Pitch** (Decimal Range) — default: `-90.0` – `90.0`; range: `-90.0` – `90.0` — Pitch angle range in which Eagle is allowed to activate.


### Screenshots

*Screenshots for Eagle will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleEagle.kt)*
