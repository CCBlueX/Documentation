## AutoF5

Automatically enables F5 mode when opening the inventory or a chest.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
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

#### CheckScreenHandlerType

A toggleable group of settings (default: enabled).

> *This is a shared settings group defined in `CheckScreenHandlerTypeValueGroup`. See also: other modules using screen handler type checks.*

- **Enabled** (Toggle) — default: `true`
- **Types** (Registry List)
- **Filter** (Choice) — default: `WHITELIST`; options: `Whitelist`, `Blacklist`

#### CheckScreenTitle

A toggleable group of settings (default: enabled).

> *This is a shared settings group defined in `CheckScreenTitleValueGroup`. See also: other modules using screen title checks.*

- **Enabled** (Toggle) — default: `true`
- **Titles** (Multi-Select) — default: `Barrel`, `Chest`, `LargeChest`, `ShulkerBox`, `ChestMinecart`; options: `Barrel`, `Beacon`, `BlastFurnace`, `BrewingStand`, `Chest`, `LargeChest`, `Dispenser`, `Dropper`, `EnderChest`, `Furnace`, `Hopper`, `ShulkerBox`, `Smoker`, `ChestMinecart`, `HopperMinecart`
- **Custom** (Editable List)
- **Filter** (Choice) — default: `WHITELIST`; options: `Whitelist`, `Blacklist`


### Screenshots

*Screenshots for AutoF5 will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleAutoF5.kt)*
