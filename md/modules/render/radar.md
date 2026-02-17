## Radar

Shows the direction of rendered entities on GUI.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Tilt (Mode Selector | default: Static | modes: Static, ByPitch)
│   ├── [Mode: Static]
│   │   └── Angle (Decimal | default: 90.0 | range: -90.0..90.0 | deg)
│   └── [Mode: ByPitch]
│       └── Limitation (Decimal Range | default: 45.0..90.0 | range: 0.0..90.0 | deg)
├── Radius (Decimal | default: 40.0 | range: 2.0..200.0)
├── OnlyPlayers (Toggle | default: false)
├── PointerMode (Mode Selector | default: Triangle | modes: Triangle, Image1, Image2)
│   ├── [Mode: Triangle]
│   │   ├── Width (Decimal | default: 8.0 | range: 1.0..100.0)
│   │   ├── Height (Decimal | default: 10.0 | range: 1.0..100.0)
│   │   └── TailConcaveSize (Decimal | default: 2.0 | range: 0.0..50.0)
│   ├── [Mode: Image1]
│   │   └── Size (Decimal | default: 10.0 | range: 1.0..100.0)
│   └── [Mode: Image2]
│       └── Size (Decimal | default: 10.0 | range: 1.0..100.0)
├── ColorMode (Mode Selector | default: Distance | modes: Distance, Health, Static, Rainbow)
│   ├── [Mode: Distance]
│   │   ├── Saturation (Decimal | default: 1.0 | range: 0.0..1.0)
│   │   ├── Brightness (Decimal | default: 1.0 | range: 0.0..1.0)
│   │   └── Hue (Curve)
│   ├── [Mode: Health]
│   │   └── Alpha (Integer | default: 255 | range: 0..255)
│   ├── [Mode: Static]
│   │   └── Color (Color)
└── Alpha (Curve)
```

### Settings Details

#### Tilt

Select a mode for this feature. Available modes: **Static**, **ByPitch**. Default: **Static**.

##### Mode: Static

- **Angle** (Decimal) — default: `90.0`; range: `-90.0` – `90.0`; unit: deg — Sets the fixed tilt angle of the radar plane.

##### Mode: ByPitch

- **Limitation** (Decimal Range) — default: `45.0` – `90.0`; range: `0.0` – `90.0`; unit: deg — Limits the pitch-based tilt range of the radar plane.

- **Radius** (Decimal) — default: `40.0`; range: `2.0` – `200.0` — Sets the distance from the screen center where pointers appear.
- **OnlyPlayers** (Toggle) — default: `false` — Only shows player entities on the radar.
#### PointerMode

Select a mode for this feature. Available modes: **Triangle**, **Image1**, **Image2**. Default: **Triangle**.

##### Mode: Triangle

- **Width** (Decimal) — default: `8.0`; range: `1.0` – `100.0` — Sets the width of the triangle pointer.
- **Height** (Decimal) — default: `10.0`; range: `1.0` – `100.0` — Sets the height of the triangle pointer.
- **TailConcaveSize** (Decimal) — default: `2.0`; range: `0.0` – `50.0` — Sets the concave depth of the triangle tail.

##### Mode: Image1

- **Size** (Decimal) — default: `10.0`; range: `1.0` – `100.0` — Sets the size of the image pointer.

##### Mode: Image2

- **Size** (Decimal) — default: `10.0`; range: `1.0` – `100.0` — Sets the size of the image pointer.

#### ColorMode

Select a mode for this feature. Available modes: **Distance**, **Health**, **Static**, **Rainbow**. Default: **Distance**.

##### Mode: Distance

- **Saturation** (Decimal) — default: `1.0`; range: `0.0` – `1.0` — Sets the color saturation for distance-based coloring.
- **Brightness** (Decimal) — default: `1.0`; range: `0.0` – `1.0` — Sets the color brightness for distance-based coloring.
- **Hue** (Curve) — Maps entity distance to a hue value.

##### Mode: Health

- **Alpha** (Integer) — default: `255`; range: `0` – `255` — Sets the transparency of health-based coloring.

##### Mode: Static

- **Color** (Color) — Sets the static color for all entity pointers.

- **Alpha** (Curve) — Controls pointer transparency based on entity distance.

### Screenshots

*Screenshots for Radar will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleRadar.kt)*
