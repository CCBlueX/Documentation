## ClickGUI

Shows you an easy to use menu to toggle and configure modules.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Scale (Decimal | default: 1.0 | range: 0.5..2.0)
├── SearchBarAutoFocus (Toggle | default: true)
├── Snapping (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── GridSize (Integer | default: 10 | range: 1..100 | px)
└── Cache (Toggle | default: true)
```

### Settings Details

- **Scale** (Decimal) — default: `1.0`; range: `0.5` – `2.0` — Controls the UI scale of the ClickGUI.
- **SearchBarAutoFocus** (Toggle) — default: `true` — Automatically focuses the search bar when opening the GUI.
#### Snapping

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables snapping of GUI elements to a grid.
- **GridSize** (Integer) — default: `10`; range: `1` – `100`; unit: px — Size of the snap grid in pixels.

- **Cache** (Toggle) — default: `true` — Caches the ClickGUI in a standalone screen for faster reopening.

### Screenshots

*Screenshots for ClickGUI will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleClickGui.kt)*
