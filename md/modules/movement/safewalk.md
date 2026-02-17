## SafeWalk

Prevents you from falling down block (as if you were sneaking).

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: Safe | modes: None, Safe, OnEdge)
    └── [Mode: OnEdge]
        ├── Distance (Decimal | default: 0.1 | range: 0.1..0.5)
        ├── Keep (Integer Range | default: 1..2 | range: 1..20 | ticks)
        ├── Mode (Choice | default: STOP | options: Stop, Invert, Center)
        ├── Sneak (Integer Range | default: 0..0 | range: 0..20 | ticks)
        └── Jump (Toggle | default: false)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **None**, **Safe**, **OnEdge**. Default: **Safe**.

##### Mode: OnEdge

- **Distance** (Decimal) — default: `0.1`; range: `0.1` – `0.5` — How close to the block edge the player must be to trigger protection.
- **Keep** (Integer Range) — default: `1` – `2`; range: `1` – `20`; unit: ticks — Number of ticks to continue overriding movement after edge detection.
- **Mode** (Choice) — default: `STOP`; options: `Stop`, `Invert`, `Center` — Behavior when on an edge: stop, invert movement, or walk to center.
- **Sneak** (Integer Range) — default: `0` – `0`; range: `0` – `20`; unit: ticks — Number of ticks to force sneaking after edge detection.
- **Jump** (Toggle) — default: `false` — Forces a jump when edge protection activates.


### Screenshots

*Screenshots for SafeWalk will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleSafeWalk.kt)*
