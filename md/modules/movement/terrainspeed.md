## TerrainSpeed

Allows you to move faster on specific surfaces.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── FastClimb (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Mode (Mode Selector | default: Motion | modes: Motion, Clip)
│       ├── [Mode: Motion]
│       │   └── Motion (Decimal | default: 0.2872 | range: 0.1..0.5)
├── IceSpeed (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Slipperiness (Decimal | default: 0.6 | range: 0.3..1.0)
│   └── Motion (Toggleable Group | default: off)
│       ├── Enabled (Toggle | default: false)
│       └── Motion (Decimal | default: 0.5 | range: 0.2..1.5)
└── WaterSpeed (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── AutoSwim (Toggle | default: true)
    ├── BaseSpeed (Setting Group)
    │   ├── Horizontal (Decimal | default: 0.44 | range: 0.1..10.0)
    │   └── Vertical (Decimal | default: 0.44 | range: 0.1..10.0)
    └── SprintSpeed (Toggleable Group | default: on)
        ├── Enabled (Toggle | default: true)
        ├── Horizontal (Decimal | default: 1.0 | range: 0.1..10.0)
        └── Vertical (Decimal | default: 1.0 | range: 0.1..10.0)
```

### Settings Details

#### FastClimb

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles the fast climb feature.
##### Mode

Select a mode for this feature. Available modes: **Motion**, **Clip**. Default: **Motion**.

###### Mode: Motion

- **Motion** (Decimal) — default: `0.2872`; range: `0.1` – `0.5` — Upward climb speed applied when on a ladder with horizontal collision.


#### IceSpeed

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles the ice speed feature.
- **Slipperiness** (Decimal) — default: `0.6`; range: `0.3` – `1.0` — Overrides the slipperiness value for ice blocks.
##### Motion

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles the additional horizontal motion multiplier on ice.
- **Motion** (Decimal) — default: `0.5`; range: `0.2` – `1.5` — Horizontal motion multiplier applied when moving on ice.


#### WaterSpeed

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles the water speed feature.
- **AutoSwim** (Toggle) — default: `true` — Automatically holds jump to swim upward when in water.
##### BaseSpeed

A group of related settings.

- **Horizontal** (Decimal) — default: `0.44`; range: `0.1` – `10.0` — Base horizontal speed in water.
- **Vertical** (Decimal) — default: `0.44`; range: `0.1` – `10.0` — Base vertical speed in water.

##### SprintSpeed

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles faster speed when sprinting in water.
- **Horizontal** (Decimal) — default: `1.0`; range: `0.1` – `10.0` — Horizontal speed when sprinting in water.
- **Vertical** (Decimal) — default: `1.0`; range: `0.1` – `10.0` — Vertical speed when sprinting in water.



### Screenshots

*Screenshots for TerrainSpeed will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2Fterrainspeed%2FModuleTerrainSpeed.kt)*
