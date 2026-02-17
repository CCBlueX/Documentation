## ReverseStep

Makes you step down blocks faster.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Instant | modes: Instant, Strict, Accelerator)
│   ├── [Mode: Instant]
│   │   ├── Ticks (Integer | default: 20 | range: 1..40 | ticks)
│   │   └── SimulateFalling (Toggle | default: false)
│   ├── [Mode: Strict]
│   │   └── Motion (Decimal | default: 1.0 | range: 0.1..5.0)
│   └── [Mode: Accelerator]
│       └── Factor (Decimal | default: 1.0 | range: 0.1..5.0)
└── MaximumFallDistance (Decimal | default: 1.0 | range: 1.0..50.0)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Instant**, **Strict**, **Accelerator**. Default: **Instant**.

##### Mode: Instant

- **Ticks** (Integer) — default: `20`; range: `1` – `40`; unit: ticks — Maximum number of ticks to simulate falling before giving up.
- **SimulateFalling** (Toggle) — default: `false` — Sends position packets for each simulated fall tick to appear more legitimate.

##### Mode: Strict

- **Motion** (Decimal) — default: `1.0`; range: `0.1` – `5.0` — Downward motion value applied each tick while falling.

##### Mode: Accelerator

- **Factor** (Decimal) — default: `1.0`; range: `0.1` – `5.0` — Multiplier applied to the player's vertical velocity each tick.

- **MaximumFallDistance** (Decimal) — default: `1.0`; range: `1.0` – `50.0` — Maximum distance the player is allowed to fall before reverse step is skipped.

### Screenshots

*Screenshots for ReverseStep will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2Fstep%2FModuleReverseStep.kt)*
