## NoEntityInteract

NoEntityInteract stops right-clicks on mobs and other entities, so you don't open a villager's trades or touch an armor stand by accident while you build, mine or fight.

Both filters have to match for a click to be blocked. By default that means right-clicking a villager or armor stand does nothing while your hand is empty or you hold shears, TNT, a water or lava bucket, cobweb or a mining tool. Holding anything else, like a sword, works as normal.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| EntityTypeFilter | Choice | Blacklist | Blacklist, Whitelist | Blacklist blocks the listed entities. Whitelist blocks every entity except the listed ones. |
| EntityTypes | Registry List | Villager, Armor Stand | | Entities used by EntityTypeFilter. |
| HoldingItemFilter | Choice | Whitelist | Blacklist, Whitelist | Whitelist blocks clicks only while you hold a listed item. Blacklist blocks clicks while you hold anything not listed. |
| HoldingItems | Registry List | Air, Shears, TNT, Water Bucket, Lava Bucket, Cobweb, mining tools | | Items used by HoldingItemFilter. Air means an empty hand. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleNoEntityInteract.kt)*
