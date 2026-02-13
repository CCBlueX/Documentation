## AutoTool

Automatically chooses the best tool in your inventory to mine a block.

**Category:** World  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── ToolSelector (Mode Selector | default: Dynamic | modes: Dynamic, Static)
│   ├── [Mode: Dynamic]
│   │   ├── IgnoreDurability (Toggle | default: false)
│   │   └── ConsiderInventory (Toggleable Group | default: off)
│   │       ├── Enabled (Toggle | default: false)
│   │       └── Constraints (Setting Group)
│   │           ├── StartDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   │           ├── ClickDelay (Integer Range | default: 2..4 | range: 0..20 | ticks)
│   │           ├── CloseDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   │           ├── MissChance (Integer Range | default: 0..0 | range: 0..100 | %)
│   │           └── Requires (Multi-Select | options: NoMovement, NoRotation)
│   └── [Mode: Static]
│       └── Slot (Integer | default: 0 | range: 0..8)
├── Filter (Choice | default: BLACKLIST | options: Whitelist, Blacklist)
├── Blocks (Registry List)
├── SilkTouchHandler (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── Filter (Choice | default: WHITELIST | options: Whitelist, Blacklist)
│   └── Blocks (Registry List)
├── SwapPreviousDelay (Integer | default: 20 | range: 1..100 | ticks)
├── RequireSneaking (Toggle | default: false)
└── RequireNearBed (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    └── Distance (Decimal | default: 10.0 | range: 3.0..50.0)
```

### Settings Details

#### ToolSelector

Select a mode for this feature. Available modes: **Dynamic**, **Static**. Default: **Dynamic**.

##### Mode: Dynamic

- **IgnoreDurability** (Toggle) — default: `false`
###### ConsiderInventory

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
###### Constraints

A group of related settings.

- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **ClickDelay** (Integer Range) — default: `2` – `4`; range: `0` – `20`; unit: ticks
- **CloseDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **MissChance** (Integer Range) — default: `0` – `0`; range: `0` – `100`; unit: %
- **Requires** (Multi-Select) — options: `NoMovement`, `NoRotation`



##### Mode: Static

- **Slot** (Integer) — default: `0`; range: `0` – `8`

- **Filter** (Choice) — default: `BLACKLIST`; options: `Whitelist`, `Blacklist`
- **Blocks** (Registry List)
#### SilkTouchHandler

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Filter** (Choice) — default: `WHITELIST`; options: `Whitelist`, `Blacklist`
- **Blocks** (Registry List)

- **SwapPreviousDelay** (Integer) — default: `20`; range: `1` – `100`; unit: ticks
- **RequireSneaking** (Toggle) — default: `false`
#### RequireNearBed

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Distance** (Decimal) — default: `10.0`; range: `3.0` – `50.0`


### Screenshots

*Screenshots for AutoTool will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2FModuleAutoTool.kt)*
