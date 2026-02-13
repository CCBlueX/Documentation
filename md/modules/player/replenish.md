## Replenish

Automatically refills your hotbar with items from your inventory when the count drops to a certain threshold.

**Category:** Player  
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
├── ItemThreshold (Integer | default: 5 | range: 0..63)
├── Delay (Integer | default: 40 | range: 0..1000 | ms)
├── Features (Multi-Select | default: [CleanUp] | options: CleanUp, UsePickupAll, UseSwap)
└── InsideOf (Multi-Select | options: Chests, Inventories)
```

### Settings Details

#### Constraints

A group of related settings. *Shared setting group — configured identically across modules that use inventory actions.*

- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **ClickDelay** (Integer Range) — default: `2` – `4`; range: `0` – `20`; unit: ticks
- **CloseDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **MissChance** (Integer Range) — default: `0` – `0`; range: `0` – `100`; unit: %
- **Requires** (Multi-Select) — options: `NoMovement`, `NoRotation`, `InventoryOpen`

- **ItemThreshold** (Integer) — default: `5`; range: `0` – `63` — Item count at or below which a hotbar slot is refilled.
- **Delay** (Integer) — default: `40`; range: `0` – `1000`; unit: ms — Milliseconds to wait between replenish actions.
- **Features** (Multi-Select) — default: `CleanUp`; options: `CleanUp`, `UsePickupAll`, `UseSwap` — Refill strategies to use (CleanUp prioritizes small stacks, UseSwap swaps full stacks, UsePickupAll merges stacks).
- **InsideOf** (Multi-Select) — options: `Chests`, `Inventories` — Allows replenishing while inside chest or inventory screens.

### Screenshots

*Screenshots for Replenish will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleReplenish.kt)*
