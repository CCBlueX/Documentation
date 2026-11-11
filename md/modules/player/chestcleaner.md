## ChestCleaner

ChestCleaner throws unwanted items out of a chest or other container when you open it. Put the items on its list and it drops them for you, so you can clear junk out of loot chests fast.

It goes well with [ChestStealer](/docs/modules/player/cheststealer), which takes the items you want, and [InventoryCleaner](/docs/modules/player/inventorycleaner), which cleans up your own inventory.

**Category:** Player
**Enabled by default:** No
**Aliases:** ContainerCleaner

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Filter | Choice | Whitelist | Whitelist, Blacklist | Whitelist drops only the items on the list. Blacklist drops everything except them. |
| Items | Registry List | | | The item list used by Filter. |
| AutoClose | Toggle | true | | Closes the container when nothing is left to drop. |
| Constraints | Setting Group | | | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| CheckScreenHandlerType | Toggleable Group | On | | See [Shared: CheckScreenHandlerType](/docs/modules/shared-settings/checkscreenhandlertype). |
| CheckScreenTitle | Toggleable Group | On | | See [Shared: CheckScreenTitle](/docs/modules/shared-settings/checkscreentitle). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleChestCleaner.kt)*
