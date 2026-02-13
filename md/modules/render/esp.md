## ESP

Highlights all targets allowing you to see them through walls.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Glow | modes: Box, 2D, Glow)
│   ├── [Mode: Box]
│   │   ├── Outline (Toggle | default: true)
│   │   └── Expand (Decimal | default: 0.05 | range: 0.0..0.5)
│   ├── [Mode: 2D]
│   │   ├── Expand (Decimal | default: 0.05 | range: 0.0..0.5)
│   │   ├── Fill (Toggle | default: true)
│   │   ├── Outline (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── Thickness (Decimal | default: 1.0 | range: 1.0..9.0 | px)
│   │   ├── Border (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── Thickness (Decimal | default: 1.0 | range: 1.0..9.0 | px)
│   │   └── HealthBar (Toggleable Group | default: on)
│   │       ├── Enabled (Toggle | default: true)
│   │       └── Spacing (Decimal | default: 2.0 | range: 0.0..32.0 | px)
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
├── Friends (Color)
└── MaximumDistance (Decimal | default: 128.0 | range: 1.0..512.0)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Box**, **2D**, **Glow**. Default: **Glow**.

##### Mode: Box

- **Outline** (Toggle) — default: `true` — Draws an outline around the ESP box.
- **Expand** (Decimal) — default: `0.05`; range: `0.0` – `0.5` — Inflates the bounding box size of entities.

##### Mode: 2D

- **Expand** (Decimal) — default: `0.05`; range: `0.0` – `0.5` — Inflates the bounding box used for 2D projection.
- **Fill** (Toggle) — default: `true` — Fills the interior of the 2D rectangle.
###### Outline

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles the colored outline around the 2D rectangle.
- **Thickness** (Decimal) — default: `1.0`; range: `1.0` – `9.0`; unit: px — Line width of the 2D outline.

###### Border

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles a dark border around the outline.
- **Thickness** (Decimal) — default: `1.0`; range: `1.0` – `9.0`; unit: px — Line width of the dark border.

###### HealthBar

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles the vertical health bar beside the 2D rectangle.
- **Spacing** (Decimal) — default: `2.0`; range: `0.0` – `32.0`; unit: px — Gap between the 2D rectangle and the health bar.


#### ColorMode

Select a mode for this feature. Available modes: **Distance**, **Health**, **Static**, **Rainbow**. Default: **Distance**.

##### Mode: Distance

- **Saturation** (Decimal) — default: `1.0`; range: `0.0` – `1.0` — HSB saturation of the distance-based color.
- **Brightness** (Decimal) — default: `1.0`; range: `0.0` – `1.0` — HSB brightness of the distance-based color.
- **Hue** (Curve) — Curve mapping distance to hue value.
- **Alpha** (Decimal) — default: `1.0`; range: `0.0` – `1.0` — Opacity of the distance-based color.

##### Mode: Health

- **Alpha** (Integer) — default: `255`; range: `0` – `255` — Opacity of the health-based color.

##### Mode: Static

- **Color** (Color) — Static color applied to all highlighted entities.

- **Friends** (Color) — Color used to highlight friend entities.
- **MaximumDistance** (Decimal) — default: `128.0`; range: `1.0` – `512.0` — Maximum render distance for highlighted entities.

### Screenshots

*Screenshots for ESP will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2Fesp%2FModuleESP.kt)*
