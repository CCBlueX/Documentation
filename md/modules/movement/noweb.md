## NoWeb

Disables slow down caused by webs.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: Air | modes: Air, Grim2365, Intave14, Strafe)
    ├── [Mode: Grim2365]
    │   └── BreakOnWorld (Toggle | default: true)
    └── [Mode: Strafe]
        ├── Strength (Decimal | default: 0.23 | range: 0.01..0.8)
        ├── MotionY (Toggleable Group | default: off)
        │   ├── Enabled (Toggle | default: false)
        │   └── MotionYStrength (Decimal | default: 0.6 | range: -2.0..2.0)
        └── OnlyOnGround (Toggle | default: false)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Air**, **Grim2365**, **Intave14**, **Strafe**. Default: **Air**.

##### Mode: Grim2365

- **BreakOnWorld** (Toggle) — default: `true` — Also removes the web block client-side to bypass BadPacketsX checks.

##### Mode: Strafe

- **Strength** (Decimal) — default: `0.23`; range: `0.01` – `0.8` — Horizontal strafe speed applied when moving through webs.
###### MotionY

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles vertical motion override while in webs.
- **MotionYStrength** (Decimal) — default: `0.6`; range: `-2.0` – `2.0` — Vertical motion value applied while in webs.

- **OnlyOnGround** (Toggle) — default: `false` — Only applies the strafe when the player is on the ground.


### Screenshots

*Screenshots for NoWeb will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2Fnoweb%2FModuleNoWeb.kt)*
