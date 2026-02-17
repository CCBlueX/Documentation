## Crosshair

liquidbounce.module.crosshair.description

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: Circle | modes: Circle)
    └── [Mode: Circle]
        ├── ShowInThirdPerson (Toggle | default: true)
        ├── Radius (Setting Group)
        │   ├── Range (Decimal Range | default: 3.0..5.0 | range: 0.0..25.0)
        │   └── DynamicRadiusMultiplier (Decimal | default: 1.0 | range: 0.0..5.0)
        └── Color (Setting Group)
            ├── Sync (Toggle | default: true)
            ├── FirstColor (Color)
            ├── SecondColor (Color)
            └── SpinSpeed (Decimal | default: 4.0 | range: -10.0..10.0)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Circle**. Default: **Circle**.

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



### Screenshots

*Screenshots for Crosshair will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2Fcrosshair%2FModuleCrosshair.kt)*
