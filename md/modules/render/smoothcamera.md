## SmoothCamera

Makes your camera move smoother.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── EnableFirstPOV (Toggle | default: false)
├── ResetOnPerspectiveChange (Toggle | default: true)
├── HorizontalFactor (Decimal | default: 0.9 | range: 0.0..1.0)
└── VerticalFactor (Decimal | default: 0.93 | range: 0.0..1.0)
```

### Settings Details

- **EnableFirstPOV** (Toggle) — default: `false` — Enables camera smoothing in first-person view.
- **ResetOnPerspectiveChange** (Toggle) — default: `true` — Resets the smooth position when the perspective changes.
- **HorizontalFactor** (Decimal) — default: `0.9`; range: `0.0` – `1.0` — Controls the horizontal smoothing intensity (higher is smoother).
- **VerticalFactor** (Decimal) — default: `0.93`; range: `0.0` – `1.0` — Controls the vertical smoothing intensity (higher is smoother).

### Screenshots

*Screenshots for SmoothCamera will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleSmoothCamera.kt)*
