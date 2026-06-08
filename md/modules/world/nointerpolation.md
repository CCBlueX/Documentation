## NoInterpolation

Reduces entity interpolation steps so that other entities' position updates appear more immediate instead of being smoothed out over several client ticks. Useful when you want enemies to snap to their real server position rather than gliding toward it.

**Category:** World
**Enabled by default:** No

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── ReduceBy (Integer | default: 3 | range: 1..3)
```

### Settings Details

- **ReduceBy** (Integer) — default: `3`; range: `1` – `3` — How many interpolation ticks to remove. Higher values make positions update more instantly; the maximum of `3` effectively disables interpolation.

### Screenshots

*Screenshots for NoInterpolation will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2FModuleNoInterpolation.kt)*
