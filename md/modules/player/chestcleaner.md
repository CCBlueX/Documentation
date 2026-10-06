## ChestCleaner

ChestCleaner automatically throws away items you don't want straight out of any open chest or container. When you open a container, it scans the contents and drops every item that matches your filter, so you can sweep junk out of loot chests without dragging each stack into the void by hand.

Use the **Filter** setting to decide how the **Items** list is read: in Whitelist mode only the items you list are dropped, while in Blacklist mode everything *except* your listed items gets dropped. Build the **Items** list to match the loot you care about. If a container holds nothing worth dropping and **AutoClose** is on, the screen closes by itself so you can move on quickly.

This module pairs naturally with [ChestStealer](/docs/modules/player/cheststealer) for grabbing what you want and [InventoryCleaner](/docs/modules/player/inventorycleaner) for tidying your own inventory afterwards. The timing of its clicks is governed by the shared inventory constraints, and you can restrict it to specific container types or titles so it doesn't fire in the wrong menu.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Filter | Choice | Whitelist | Whitelist, Blacklist | Whether the Items list is treated as a whitelist (only listed items are dropped) or a blacklist (everything except listed items is dropped). |
| Items | Registry List | — | — | The items this module looks for, interpreted according to the Filter mode. |
| AutoClose | Toggle | true | — | Closes the container automatically once there is nothing left to drop. |
| Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| CheckScreenHandlerType | Toggleable Group | on | — | See [Shared: CheckScreenHandlerType](/docs/modules/shared-settings/checkscreenhandlertype). |
| CheckScreenTitle | Toggleable Group | on | — | See [Shared: CheckScreenTitle](/docs/modules/shared-settings/checkscreentitle). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleChestCleaner.kt)*
