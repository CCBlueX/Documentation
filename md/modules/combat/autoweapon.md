## AutoWeapon

Automatically selects the best weapon in your hotbar.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Preferred (Choice | default: SWORD | options: Any, Knockback, Sword, Axe, Mace, Spear, None)
├── AutoShieldBreak (Toggle | default: true)
├── AutoMace (Toggle | default: true)
├── SwitchBack (Integer | default: 20 | range: 1..300 | ticks)
└── ChangeOn (Multi-Select | default: [OnAttack] | options: OnAttack, OnTarget)
```

### Settings Details

- **Preferred** (Choice) — default: `SWORD`; options: `Any`, `Knockback`, `Sword`, `Axe`, `Mace`, `Spear`, `None` — Preferred weapon type to select from the hotbar.
- **AutoShieldBreak** (Toggle) — default: `true` — Automatically switches to an axe when the target is blocking with a shield.
- **AutoMace** (Toggle) — default: `true` — Automatically switches to a mace when a smash attack is possible.
- **SwitchBack** (Integer) — default: `20`; range: `1` – `300`; unit: ticks — Ticks before reverting to the previous hotbar slot after switching.
- **ChangeOn** (Multi-Select) — default: `OnAttack`; options: `OnAttack`, `OnTarget` — When to switch weapons: on attack or when a target is acquired.

### Screenshots

*Screenshots for AutoWeapon will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleAutoWeapon.kt)*
