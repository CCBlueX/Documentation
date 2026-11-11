## Inventory Constraints

Inventory Constraints control how modules move items in your inventory or in chests. Real players need a moment for each click, and anticheats notice clicks that are too fast. These settings add small waits between clicks and can stop the module while you are doing other things.

Modules that move items use this group, for example AutoArmor, ChestStealer, InventoryCleaner and Offhand.

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| StartDelay | Integer Range | 1..2 | 0..20 ticks | How long to wait after opening the inventory before the first click, in ticks (20 per second). |
| ClickDelay | Integer Range | 2..4 | 0..20 ticks | How long to wait between clicks. |
| CloseDelay | Integer Range | 1..2 | 0..20 ticks | How long to wait after the last click before closing the inventory. |
| MissChance | Integer Range | 0..0 | 0..100 % | How often to click a wrong slot first, like a real player missing. Only in chests. |
| Requires | Multi-Select | | NoMovement, NoRotation, NotUsingItem, NotBreaking, NotDuringCombat, InventoryOpen | Only clicks when all picked conditions are true. NoMovement: you are not walking or jumping. NoRotation: you are not turning. NotUsingItem: you are not eating, drinking or blocking. NotBreaking: you are not mining. NotDuringCombat: you are not fighting. InventoryOpen: your inventory is open. |

InventoryOpen is only there in modules that sort your own inventory, like [AutoArmor](/docs/modules/combat/autoarmor) and [InventoryCleaner](/docs/modules/player/inventorycleaner). Without it, the client opens your inventory without you seeing it when the server's version allows that.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/inventory/InventoryValueGroups.kt)*
