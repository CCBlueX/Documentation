## Crosshair

Changes the style of your crosshair.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: Circle | modes: Circle, CS2)
    ├── [Mode: Circle]
    │   ├── ShowInThirdPerson (Toggle | default: true)
    │   ├── Radius (Setting Group)
    │   │   ├── Range (Decimal Range | default: 3.0..5.0 | range: 0.0..25.0)
    │   │   └── DynamicRadiusMultiplier (Decimal | default: 1.0 | range: 0.0..5.0)
    │   └── Color (Setting Group)
    │       ├── Sync (Toggle | default: true)
    │       ├── FirstColor (Color)
    │       ├── SecondColor (Color)
    │       └── SpinSpeed (Decimal | default: 4.0 | range: -10.0..10.0)
    └── [Mode: CS2]
        ├── ShowInThirdPerson (Toggle | default: true)
        ├── Crosshair (Setting Group)
        │   ├── Length (Decimal | default: 5.0 | range: 1.0..20.0)
        │   ├── Thickness (Decimal | default: 1.0 | range: 0.5..5.0)
        │   ├── Gap (Decimal | default: 2.0 | range: 0.0..10.0)
        │   └── DynamicMultiplier (Decimal | default: 1.0 | range: 0.0..10.0)
        └── Color (Setting Group)
            ├── Sync (Toggle | default: true)
            ├── FirstColor (Color)
            ├── SecondColor (Color)
            └── SpinSpeed (Decimal | default: 4.0 | range: -10.0..10.0)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Circle**, **CS2**. Default: **Circle**.

##### Mode: Circle

- **ShowInThirdPerson** (Toggle) — default: `true` — Displays the custom crosshair even in third-person view.
###### Radius

A group of related settings.

- **Range** (Decimal Range) — default: `3.0` – `5.0`; range: `0.0` – `25.0` — Inner and outer radius of the crosshair circle.
- **DynamicRadiusMultiplier** (Decimal) — default: `1.0`; range: `0.0` – `5.0` — Multiplier for radius expansion based on attack cooldown.

###### Color

A group of related settings.

- **Sync** (Toggle) — default: `true` — Uses the first color for both ends of the gradient.
- **FirstColor** (Color) — Primary color of the crosshair gradient.
- **SecondColor** (Color) — Secondary color of the crosshair gradient when Sync is off.
- **SpinSpeed** (Decimal) — default: `4.0`; range: `-10.0` – `10.0` — Speed and direction of the color gradient rotation.

##### Mode: CS2

A flat four-line crosshair in the style of Counter-Strike 2, with an adjustable gap that can expand dynamically.

- **ShowInThirdPerson** (Toggle) — default: `true` — Displays the custom crosshair even in third-person view.

###### Crosshair

- **Length** (Decimal) — default: `5.0`; range: `1.0` – `20.0` — Length of each crosshair line.
- **Thickness** (Decimal) — default: `1.0`; range: `0.5` – `5.0` — Thickness of each line.
- **Gap** (Decimal) — default: `2.0`; range: `0.0` – `10.0` — Gap between the center and the start of each line.
- **DynamicMultiplier** (Decimal) — default: `1.0`; range: `0.0` – `10.0` — How much the gap expands based on attack cooldown / movement.

###### Color

- **Sync** (Toggle) — default: `true` — Uses the first color for both ends of the gradient.
- **FirstColor** (Color) — Primary color of the crosshair.
- **SecondColor** (Color) — Secondary color when Sync is off.
- **SpinSpeed** (Decimal) — default: `4.0`; range: `-10.0` – `10.0` — Speed and direction of the color gradient rotation.

### Screenshots

*Screenshots for Crosshair will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2Fcrosshair%2FModuleCrosshair.kt)*
