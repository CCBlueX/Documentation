## InventoryCleaner

InventoryCleaner sorts your inventory for you. It puts the items you choose into each hotbar slot and your offhand, merges half-full stacks, and throws away items you don't need.

Pick an item type for each hotbar slot with the SlotItem settings. The Maximum settings decide how much of something to keep, and anything over that gets dropped. Set one to 0 to throw all of that item away. Items in ItemsBlacklist are always thrown out. Your armor is left alone (use [AutoArmor](/docs/modules/combat/autoarmor) for that), and so is your offhand while [Offhand](/docs/modules/player/offhand) is running.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Constraints | Setting Group | | | See [Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| MaximumBlocks | Integer | 512 | 0..2500 | Most blocks to keep. |
| MaximumArrows | Integer | 128 | 0..2500 | Most arrows to keep, all kinds together. |
| MaximumThrowables | Integer | 64 | 0..600 | Most throwable items (snowballs, eggs, wind charges) to keep. |
| MaximumFoodPoints | Integer | 200 | 0..2000 | Most food to keep, counted in hunger points it fills. |
| MaximumWaterBuckets | Integer | 2 | 0..16 | Most water buckets to keep. |
| MaximumLavaBuckets | Integer | 2 | 0..16 | Most lava buckets to keep. |
| MaximumMilkBuckets | Integer | 2 | 0..16 | Most milk buckets to keep. |
| ItemsBlacklist | Registry List | None | | Items that are always thrown out. |
| Greedy | Toggle | On | | Swaps an item in a slot for a better one of the same type from your inventory. |
| OffHandItem | Choice | Shield | | Item type for your offhand. |
| SlotItem-1 | Choice | Weapon | | Item type for hotbar slot 1. |
| SlotItem-2 | Choice | Bow | | Item type for hotbar slot 2. |
| SlotItem-3 | Choice | Pickaxe | | Item type for hotbar slot 3. |
| SlotItem-4 | Choice | Axe | | Item type for hotbar slot 4. |
| SlotItem-5 | Choice | None | | Item type for hotbar slot 5. |
| SlotItem-6 | Choice | Potion | | Item type for hotbar slot 6. |
| SlotItem-7 | Choice | Food | | Item type for hotbar slot 7. |
| SlotItem-8 | Choice | Block | | Item type for hotbar slot 8. |
| SlotItem-9 | Choice | Block | | Item type for hotbar slot 9. |

Item types for the slot and offhand settings: `Sword`, `Weapon`, `Spear`, `Mace`, `BestKnockback`, `Bow`, `Crossbow`, `Axe`, `Pickaxe`, `Shovel`, `Hoe`, `Rod`, `Shield`, `Water`, `Lava`, `Milk`, `Pearl`, `Gapple`, `Food`, `Potion`, `Block`, `Throwables`, `Ignore` (leave the slot alone) and `None` (any item can go there).

An axe with Sharpness V or higher counts as a weapon. Other axes count as tools.

`BestKnockback` keeps your best Knockback item, like a knockback stick, in its own slot. It only takes items with more Knockback than your best weapon.


---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/invcleaner/ModuleInventoryCleaner.kt)*
