## Sprint

Makes you sprint automatically.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Choice | default: LEGIT | options: Legit, Omnidirectional, Omnirotational)
├── Ignore (Multi-Select | options: Blindness, Hunger, Collision)
└── StopOn (Multi-Select | default: [Ground, Air, UsingItem] | options: Ground, Air, UsingItem)
```

### Settings Details

- **Mode** (Choice) — default: `LEGIT`; options: `Legit`, `Omnidirectional`, `Omnirotational` — Sprint behavior: Legit (forward only), Omnidirectional (all directions), or Omnirotational (rotates view).
- **Ignore** (Multi-Select) — options: `Blindness`, `Hunger`, `Collision` — Conditions to ignore that would normally prevent sprinting.
- **StopOn** (Multi-Select) — default: `Ground`, `Air`, `UsingItem`; options: `Ground`, `Air`, `UsingItem` — Situations where sprinting should be stopped when not moving forward.

### Screenshots

*Screenshots for Sprint will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleSprint.kt)*
