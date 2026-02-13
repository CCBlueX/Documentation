## KeepSprint

Keeps you sprinting even when attacking.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Motion (Decimal Range | default: 100.0..100.0 | range: 0.0..100.0 | %)
├── MotionWhenHurt (Decimal Range | default: 100.0..100.0 | range: 0.0..100.0 | %)
├── HurtTime (Integer Range | default: 1..10 | range: 1..10)
└── Chance (Decimal | default: 100.0 | range: 0.0..100.0 | %)
```

### Settings Details

- **Motion** (Decimal Range) — default: `100.0` – `100.0`; range: `0.0` – `100.0`; unit: % — Percentage of motion retained after hitting an entity (100% = no slowdown).
- **MotionWhenHurt** (Decimal Range) — default: `100.0` – `100.0`; range: `0.0` – `100.0`; unit: % — Percentage of motion retained when the player is in their hurt animation.
- **HurtTime** (Integer Range) — default: `1` – `10`; range: `1` – `10` — Hurt-time range during which MotionWhenHurt applies instead of Motion.
- **Chance** (Decimal) — default: `100.0`; range: `0.0` – `100.0`; unit: % — Probability that sprint is kept on each hit.

### Screenshots

*Screenshots for KeepSprint will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleKeepSprint.kt)*
