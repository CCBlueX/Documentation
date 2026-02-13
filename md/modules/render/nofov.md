## NoFOV

Disables FOV from changing during movement

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: Constant | modes: Constant, Custom)
    ├── [Mode: Constant]
    │   └── FOV (Integer | default: 90 | range: 1..179)
    └── [Mode: Custom]
        ├── BaseFOV (Decimal | default: 1.0 | range: 0.0..1.5)
        ├── Limit (Decimal Range | default: 0.0..1.5 | range: 0.0..1.5)
        └── Multiplier (Decimal | default: 1.0 | range: 0.1..1.5)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Constant**, **Custom**. Default: **Constant**.

##### Mode: Constant

- **FOV** (Integer) — default: `90`; range: `1` – `179` — Sets the fixed field of view value.

##### Mode: Custom

- **BaseFOV** (Decimal) — default: `1.0`; range: `0.0` – `1.5` — Sets the base FOV multiplier before adjustments.
- **Limit** (Decimal Range) — default: `0.0` – `1.5`; range: `0.0` – `1.5` — Clamps the resulting FOV multiplier within this range.
- **Multiplier** (Decimal) — default: `1.0`; range: `0.1` – `1.5` — Scales the dynamic FOV change amount.


### Screenshots

*Screenshots for NoFOV will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleNoFov.kt)*
