## AutoArmor

Automatically equips the best armor in your inventory.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Constraints (Setting Group)
│   ├── StartDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   ├── ClickDelay (Integer Range | default: 2..4 | range: 0..20 | ticks)
│   ├── CloseDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   ├── MissChance (Integer Range | default: 0..0 | range: 0..100 | %)
│   └── Requires (Multi-Select | options: NoMovement, NoRotation, InventoryOpen)
├── Hotbar (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── CanSwapArmor (Toggle | default: false)
└── SaveArmor (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── DurabilityThreshold (Integer | default: 24 | range: 0..100)
    └── AutoOpenInventory (Toggle | default: true)
```

### Settings Details

#### Constraints

A group of related settings.

- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks — Delay before starting inventory actions.
- **ClickDelay** (Integer Range) — default: `2` – `4`; range: `0` – `20`; unit: ticks — Delay between inventory click actions.
- **CloseDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks — Delay before closing the inventory after actions.
- **MissChance** (Integer Range) — default: `0` – `0`; range: `0` – `100`; unit: % — Chance to intentionally miss a click to appear more human-like.
- **Requires** (Multi-Select) — options: `NoMovement`, `NoRotation`, `InventoryOpen` — Conditions that must be met before the module performs actions.

#### Hotbar

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **CanSwapArmor** (Toggle) — default: `false` — Allows armor swapping via hotbar (MC 1.19.4+); requires Hotbar to be enabled.

#### SaveArmor

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **DurabilityThreshold** (Integer) — default: `24`; range: `0` – `100` — Minimum durability percentage before armor is considered for replacement.
- **AutoOpenInventory** (Toggle) — default: `true` — Automatically opens the inventory when armor needs to be saved.


### Screenshots

*Screenshots for AutoArmor will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleAutoArmor.kt)*
