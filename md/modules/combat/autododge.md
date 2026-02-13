## AutoDodge

Automatically dodges projectiles like arrows.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Ignore (Multi-Select | default: [OpenInventory, UsingItem, UsingScaffold] | options: OpenInventory, UsingItem, UsingScaffold)
├── AllowRotationChange (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   └── AllowJump (Toggle | default: true)
└── AllowTimer (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    └── TimerSpeed (Decimal | default: 2.0 | range: 1.0..10.0 | x)
```

### Settings Details

- **Ignore** (Multi-Select) — default: `OpenInventory`, `UsingItem`, `UsingScaffold`; options: `OpenInventory`, `UsingItem`, `UsingScaffold` — Conditions under which dodging is suppressed.
#### AllowRotationChange

A toggleable group of settings (default: disabled). When enabled, allows the module to change your look direction to dodge.

- **Enabled** (Toggle) — default: `false` — Enables rotation changes while dodging.
- **AllowJump** (Toggle) — default: `true` — Allows jumping as part of the dodge maneuver.

#### AllowTimer

A toggleable group of settings (default: disabled). When enabled, uses timer speed-up to dodge faster.

- **Enabled** (Toggle) — default: `false` — Enables timer-based dodge acceleration.
- **TimerSpeed** (Decimal) — default: `2.0`; range: `1.0` – `10.0`; unit: x — Game speed multiplier applied while dodging.


### Screenshots

*Screenshots for AutoDodge will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleAutoDodge.kt)*
