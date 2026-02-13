## BlockOutline

Changes the way Minecraft highlights blocks.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── SideOnly (Toggle | default: true)
├── Color (Color)
├── Outline (Color)
└── Slide (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── Time (Integer | default: 150 | range: 1..1000 | ms)
    └── Easing (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
```

### Settings Details

- **SideOnly** (Toggle) — default: `true` — Highlights only the targeted face of the block instead of the full outline.
- **Color** (Color) — Fill color of the block highlight.
- **Outline** (Color) — Outline color of the block highlight.
#### Slide

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables the sliding transition between block highlights.
- **Time** (Integer) — default: `150`; range: `1` – `1000`; unit: ms — Duration of the slide animation between targeted blocks.
- **Easing** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None` — Easing function for the slide transition.


### Screenshots

*Screenshots for BlockOutline will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleBlockOutline.kt)*
