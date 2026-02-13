## Debug

Only of interest to developers.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Parameters (Toggle | default: true)
├── Geometry (Toggle | default: true)
├── Expires (Integer | default: 5 | range: 1..30 | secs)
├── SimulatedPlayer (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   └── TicksToPredict (Integer | default: 20 | range: 5..100)
└── Graph (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    └── Curve (Curve)
```

### Settings Details

- **Parameters** (Toggle) — default: `true` — Enables the on-screen overlay of debug parameter values.
- **Geometry** (Toggle) — default: `true` — Enables rendering of debug geometry shapes in the world.
- **Expires** (Integer) — default: `5`; range: `1` – `30`; unit: secs — Time before debug parameter entries are removed.
#### SimulatedPlayer

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles rendering of the simulated player movement path.
- **TicksToPredict** (Integer) — default: `20`; range: `5` – `100` — Number of ticks to simulate ahead for player position prediction.

#### Graph

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles the curve graph overlay on screen.
- **Curve** (Curve) — Defines the data points plotted on the graph overlay.


### Screenshots

*Screenshots for Debug will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleDebug.kt)*
