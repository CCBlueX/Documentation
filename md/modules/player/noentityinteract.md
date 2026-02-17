## NoEntityInteract

Prevents you from interacting with entities.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── EntityTypeFilter (Choice | default: BLACKLIST | options: Whitelist, Blacklist)
├── EntityTypes (Registry List)
├── HoldingItemFilter (Choice | default: WHITELIST | options: Whitelist, Blacklist)
└── HoldingItems (Registry List)
```

### Settings Details

- **EntityTypeFilter** (Choice) — default: `BLACKLIST`; options: `Whitelist`, `Blacklist` — Whether to use the entity type list as a whitelist or blacklist.
- **EntityTypes** (Registry List) — Entity types to filter (default includes Villager and Armor Stand).
- **HoldingItemFilter** (Choice) — default: `WHITELIST`; options: `Whitelist`, `Blacklist` — Whether to use the held item list as a whitelist or blacklist.
- **HoldingItems** (Registry List) — Items that trigger skipping entity interaction when held (default includes tools, shears, TNT, etc.).

### Screenshots

*Screenshots for NoEntityInteract will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleNoEntityInteract.kt)*
