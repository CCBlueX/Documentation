## ChestCleaner

Automatically drops unwanted items from a chest.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Filter (Choice | default: WHITELIST | options: Whitelist, Blacklist)
├── Items (Registry List)
├── AutoClose (Toggle | default: true)
├── Constraints (Setting Group)
│   ├── StartDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   ├── ClickDelay (Integer Range | default: 2..4 | range: 0..20 | ticks)
│   ├── CloseDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   ├── MissChance (Integer Range | default: 0..0 | range: 0..100 | %)
│   └── Requires (Multi-Select | options: NoMovement, NoRotation, InventoryOpen)
├── CheckScreenHandlerType (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Types (Registry List)
│   └── Filter (Choice | default: WHITELIST | options: Whitelist, Blacklist)
└── CheckScreenTitle (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── Titles (Multi-Select | default: [Barrel, Chest, LargeChest, ShulkerBox, ChestMinecart] | options: Barrel, Beacon, BlastFurnace, BrewingStand, Chest, LargeChest, Dispenser, Dropper, EnderChest, Furnace, Hopper, ShulkerBox, Smoker, ChestMinecart, HopperMinecart)
    ├── Custom (Editable List)
    └── Filter (Choice | default: WHITELIST | options: Whitelist, Blacklist)
```

### Settings Details

- **Filter** (Choice) — default: `WHITELIST`; options: `Whitelist`, `Blacklist`
- **Items** (Registry List)
- **AutoClose** (Toggle) — default: `true`
#### Constraints

A group of related settings.

- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **ClickDelay** (Integer Range) — default: `2` – `4`; range: `0` – `20`; unit: ticks
- **CloseDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **MissChance** (Integer Range) — default: `0` – `0`; range: `0` – `100`; unit: %
- **Requires** (Multi-Select) — options: `NoMovement`, `NoRotation`, `InventoryOpen`

#### CheckScreenHandlerType

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Types** (Registry List)
- **Filter** (Choice) — default: `WHITELIST`; options: `Whitelist`, `Blacklist`

#### CheckScreenTitle

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Titles** (Multi-Select) — default: `Barrel`, `Chest`, `LargeChest`, `ShulkerBox`, `ChestMinecart`; options: `Barrel`, `Beacon`, `BlastFurnace`, `BrewingStand`, `Chest`, `LargeChest`, `Dispenser`, `Dropper`, `EnderChest`, `Furnace`, `Hopper`, `ShulkerBox`, `Smoker`, `ChestMinecart`, `HopperMinecart`
- **Custom** (Editable List)
- **Filter** (Choice) — default: `WHITELIST`; options: `Whitelist`, `Blacklist`


### Screenshots

*Screenshots for ChestCleaner will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleChestCleaner.kt)*
