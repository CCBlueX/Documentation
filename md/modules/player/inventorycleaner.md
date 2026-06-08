## InventoryCleaner

InventoryCleaner automatically organises your inventory while you play. It moves items into the hotbar slots you configure, merges partial stacks together to free up space, and throws out anything it considers surplus — all without you having to open your inventory manually. This makes it especially useful in fast-paced scenarios such as PvP or [Scaffold](/docs/modules/world/scaffold) bridging, where a tidy hotbar directly affects your reaction time.

You control exactly what goes where by assigning an item category to each of the nine hotbar slots and the off-hand. Any item type not assigned to a slot — and not needed to satisfy a quantity limit — will be dropped. If [Offhand](/docs/modules/player/offhand) is active at the same time, InventoryCleaner leaves the off-hand slot alone so the two modules do not conflict. Armor slots are also left untouched; use [AutoArmor](/docs/modules/combat/autoarmor) for those.

Quantity caps let you decide how much of a given consumable type to keep. Once the cap is reached, excess items are discarded. Setting a cap to its maximum value effectively means "keep everything of that type", while setting it to 0 tells the module to throw all of them away.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| MaximumBlocks | Integer | 512 | 0–2500 | Maximum number of block items to keep. Surplus blocks are dropped. |
| MaximumArrows | Integer | 128 | 0–2500 | Maximum number of arrows to keep across all arrow types. |
| MaximumThrowables | Integer | 64 | 0–600 | Maximum number of throwable items (snowballs, eggs, wind charges) to keep. |
| MaximumFoodPoints | Integer | 200 | 0–2000 | Maximum total food nutrition points worth of food items to keep. |
| Greedy | Toggle | true | — | When enabled, the module replaces items already in a hotbar slot with a better version of the same category if one is available in your inventory. |
| OffHandItem | Choice | Shield | — | Item category to place in the off-hand slot. |
| SlotItem-1 | Choice | Weapon | — | Item category to place in hotbar slot 1. |
| SlotItem-2 | Choice | Bow | — | Item category to place in hotbar slot 2. |
| SlotItem-3 | Choice | Pickaxe | — | Item category to place in hotbar slot 3. |
| SlotItem-4 | Choice | Axe | — | Item category to place in hotbar slot 4. |
| SlotItem-5 | Choice | None | — | Item category to place in hotbar slot 5. |
| SlotItem-6 | Choice | Potion | — | Item category to place in hotbar slot 6. |
| SlotItem-7 | Choice | Food | — | Item category to place in hotbar slot 7. |
| SlotItem-8 | Choice | Block | — | Item category to place in hotbar slot 8. |
| SlotItem-9 | Choice | Block | — | Item category to place in hotbar slot 9. |

Available item categories for slot and off-hand settings: `Sword`, `Weapon`, `Spear`, `Mace`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore` (leave slot untouched), `None` (no preference, slot may be used for overflow).

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/invcleaner/ModuleInventoryCleaner.kt)*
