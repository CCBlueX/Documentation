## Replenish

Replenish refills your hotbar from your inventory. When a stack in your hotbar gets down to ItemThreshold items or fewer, it moves more of the same item over. This helps when you use up a lot of one thing, like blocks with [Scaffold](/docs/modules/world/scaffold), food or potions.

It also remembers what was in each slot, so a slot you used up completely gets filled again. By default it only works while no inventory or chest is open. Use InsideOf to let it run there too.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Constraints | Setting Group | | | See [Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| ItemThreshold | Integer | 5 | 0..63 | Refills a hotbar stack once it has this many items or fewer. |
| Delay | Integer | 40 | 0..1000 ms | Time to wait between refills. |
| ReplenishEmpty | Toggle | On | | Also refills slots that ran out completely, using the item that was there last. |
| Features | Multi-Select | CleanUp | CleanUp, UsePickupAll, UseSwap | CleanUp uses up small stacks first. UsePickupAll collects matching items onto the slot in one click. UseSwap swaps a bigger stack straight into the slot. |
| InsideOf | Multi-Select | None | Chests, Inventories | Lets Replenish run while a chest or your own inventory is open. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleReplenish.kt)*
