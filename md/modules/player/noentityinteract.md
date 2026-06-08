## NoEntityInteract

NoEntityInteract prevents your client from registering right-click interactions with entities when your crosshair is aimed at them. This is useful in situations where you want to avoid accidentally opening a villager's trade menu, mounting a horse, or triggering other entity interactions while performing other actions — for example, when placing blocks, mining, or fighting near entities you don't intend to engage with.

The module provides two independent filters that both must pass for an interaction to be blocked. The **entity type filter** controls which entity types are affected, defaulting to a blacklist covering villagers and armor stands. The **holding item filter** controls which items in your main hand trigger the block, defaulting to a whitelist that includes empty hand, shears, TNT, buckets, cobweb, and all mining tools — so the module only activates when holding those items, leaving normal interaction intact when you're holding a sword or other gear.

You can freely adjust both filters to match your play style: switch either to the opposite mode, or add and remove entries to target exactly the entities and held items you care about. For a similar module that suppresses block interactions instead of entity interactions, see [NoBlockInteract](/docs/modules/player/noblockinteract).

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| EntityTypeFilter | Choice | Blacklist | — | Determines how the EntityTypes list is applied. `Blacklist` blocks interaction with the listed entity types; `Whitelist` allows interaction only with the listed entity types. |
| EntityTypes | Registry List | — | — | The entity types checked by EntityTypeFilter. Defaults to Villager and Armor Stand. |
| HoldingItemFilter | Choice | Whitelist | — | Determines how the HoldingItems list is applied. `Whitelist` blocks interaction only when holding a listed item; `Blacklist` blocks interaction when holding any item not in the list. |
| HoldingItems | Registry List | — | — | The items checked by HoldingItemFilter. Defaults to empty hand, Shears, TNT, Water Bucket, Lava Bucket, Cobweb, and all mining tools. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleNoEntityInteract.kt)*
