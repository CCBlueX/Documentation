## Vomit

Vomit items out of your inventory.

**Category:** Fun  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Constraints (Setting Group)
    ├── StartDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
    ├── ClickDelay (Integer Range | default: 2..4 | range: 0..20 | ticks)
    ├── CloseDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
    ├── MissChance (Integer Range | default: 0..0 | range: 0..100 | %)
    └── Requires (Multi-Select | options: NoMovement, NoRotation, InventoryOpen)
```

### Settings Details

#### Constraints

A group of related settings.

- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **ClickDelay** (Integer Range) — default: `2` – `4`; range: `0` – `20`; unit: ticks
- **CloseDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **MissChance** (Integer Range) — default: `0` – `0`; range: `0` – `100`; unit: %
- **Requires** (Multi-Select) — options: `NoMovement`, `NoRotation`, `InventoryOpen`


### Screenshots

*Screenshots for Vomit will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Ffun%2FModuleVomit.kt)*
