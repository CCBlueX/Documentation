## Zoom

Allows you to make everything in your world appear smaller or bigger.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Zoom (Integer | default: 30 | range: 10..150)
├── Scroll (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Speed (Decimal | default: 2.0 | range: 0.5..8.0)
├── Transition (Choice | default: QUAD_IN | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
└── DurationFactor (Decimal | default: 2.0 | range: 0.0..10.0 | x)
```

### Settings Details

- **Zoom** (Integer) — default: `30`; range: `10` – `150` — Sets the target FOV when zoomed in.
#### Scroll

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables scroll wheel to adjust the zoom level.
- **Speed** (Decimal) — default: `2.0`; range: `0.5` – `8.0` — Sets the scroll wheel zoom adjustment speed.

- **Transition** (Choice) — default: `QUAD_IN`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None` — Selects the easing function for zoom transitions.
- **DurationFactor** (Decimal) — default: `2.0`; range: `0.0` – `10.0`; unit: x — Scales the zoom transition animation duration.

### Screenshots

*Screenshots for Zoom will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleZoom.kt)*
