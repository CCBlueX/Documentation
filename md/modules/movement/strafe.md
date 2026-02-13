## Strafe

Allows you to strafe while being in mid-air.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── StrengthInAir (Decimal | default: 1.0 | range: 0.0..1.0)
├── StrengthOnGround (Decimal | default: 1.0 | range: 0.0..1.0)
└── StrictMovement (Toggle | default: false)
```

### Settings Details

- **StrengthInAir** (Decimal) — default: `1.0`; range: `0.0` – `1.0` — Strafe strength applied when the player is in the air.
- **StrengthOnGround** (Decimal) — default: `1.0`; range: `0.0` – `1.0` — Strafe strength applied when the player is on the ground.
- **StrictMovement** (Toggle) — default: `false` — Zeroes horizontal movement when the player is not providing input.

### Screenshots

*Screenshots for Strafe will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleStrafe.kt)*
