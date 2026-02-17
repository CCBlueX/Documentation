## Tracers

Draws a line to targets within a certain radius.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── ColorMode (Mode Selector | default: Distance | modes: Distance, Health, Static, Rainbow)
│   ├── [Mode: Distance]
│   │   ├── Saturation (Decimal | default: 1.0 | range: 0.0..1.0)
│   │   ├── Brightness (Decimal | default: 1.0 | range: 0.0..1.0)
│   │   ├── Hue (Curve)
│   │   └── Alpha (Decimal | default: 1.0 | range: 0.0..1.0)
│   ├── [Mode: Health]
│   │   └── Alpha (Integer | default: 255 | range: 0..255)
│   ├── [Mode: Static]
│   │   └── Color (Color)
├── LineWidth (Decimal | default: 1.0 | range: 1.0..16.0)
└── MaximumDistance (Decimal | default: 128.0 | range: 1.0..512.0)
```

### Settings Details

#### ColorMode

Select a mode for this feature. Available modes: **Distance**, **Health**, **Static**, **Rainbow**. Default: **Distance**.

##### Mode: Distance

- **Saturation** (Decimal) — default: `1.0`; range: `0.0` – `1.0` — Sets the color saturation for distance-based coloring.
- **Brightness** (Decimal) — default: `1.0`; range: `0.0` – `1.0` — Sets the color brightness for distance-based coloring.
- **Hue** (Curve) — Maps entity distance to a hue value.
- **Alpha** (Decimal) — default: `1.0`; range: `0.0` – `1.0` — Sets the transparency for distance-based coloring.

##### Mode: Health

- **Alpha** (Integer) — default: `255`; range: `0` – `255` — Sets the transparency of health-based coloring.

##### Mode: Static

- **Color** (Color) — Sets the static color for all tracer lines.

- **LineWidth** (Decimal) — default: `1.0`; range: `1.0` – `16.0` — Sets the thickness of tracer lines.
- **MaximumDistance** (Decimal) — default: `128.0`; range: `1.0` – `512.0` — Sets the maximum distance for drawing tracers to entities.

### Screenshots

*Screenshots for Tracers will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleTracers.kt)*
