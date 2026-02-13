## AirPlace

Allows you to place blocks in mid-air.

**Category:** World  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── PlaceInLiquid (Toggle | default: false)
├── Preview (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── OutlineOnly (Toggle | default: false)
│   ├── Color (Color)
│   └── OutlineColor (Color)
└── CustomRange (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── Range (Decimal | default: 3.0 | range: 1.0..4.5)
    └── ScrollAdjust (Toggleable Group | default: on)
        ├── Enabled (Toggle | default: true)
        ├── Modifier (Key)
        └── Sensitivity (Decimal | default: 0.5 | range: 0.1..1.0)
```

### Settings Details

- **PlaceInLiquid** (Toggle) — default: `false`
#### Preview

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **OutlineOnly** (Toggle) — default: `false`
- **Color** (Color)
- **OutlineColor** (Color)

#### CustomRange

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Range** (Decimal) — default: `3.0`; range: `1.0` – `4.5`
##### ScrollAdjust

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Modifier** (Key)
- **Sensitivity** (Decimal) — default: `0.5`; range: `0.1` – `1.0`



### Screenshots

*Screenshots for AirPlace will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2FModuleAirPlace.kt)*
