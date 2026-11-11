## AutoDeposit

AutoDeposit puts items from your inventory into a chest, barrel or shulker box for you. Open the container and it moves every item that matches your list. It works the other way round from [ChestStealer](/docs/modules/player/cheststealer). Use it to empty a full inventory into your storage room.

With **PunchToDeposit** you can also hit a chest to put an item from your hotbar into it without opening it.

**Category:** Player
**Enabled by default:** No
**Aliases:** AutoStore, ContainerStorer

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Filter | Choice | Whitelist | Whitelist, Blacklist | Whitelist puts in only the items on the list. Blacklist puts in everything except them. |
| Items | Registry List | | | The item list used by Filter. |
| AutoClose | Toggle | true | | Closes the container when nothing is left to put in. Only for containers it has put items into. |
| Constraints | Setting Group | | | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| CheckScreenHandlerType | Toggleable Group | On | | See [Shared: CheckScreenHandlerType](/docs/modules/shared-settings/checkscreenhandlertype). |
| CheckScreenTitle | Toggleable Group | On | | See [Shared: CheckScreenTitle](/docs/modules/shared-settings/checkscreentitle). |
| PunchToDeposit | Toggleable Group | Off | | Hit a storage block to put a stack from your hotbar into it. |
| PunchToDeposit → Range | Decimal | 3.0 | 1.0..6.0 | How far away the block can be, in blocks. |
| PunchToDeposit → WallRange | Decimal | 0.0 | 0.0..6.0 | How far away a block behind a wall can be. Can't be more than Range. |
| PunchToDeposit → Delay | Integer | 5 | 1..80 ticks | Wait between hits, in ticks (20 per second). |
| PunchToDeposit → SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Whether your arm swing is shown, and to whom. |
| PunchToDeposit → PauseOn | Multi-Select | | Combat, UsingItem | Pauses while you are fighting or using an item. |
| PunchToDeposit → ValidStorageBlocks | Registry List | Chest, Ender Chest | | Blocks you can hit to put items in. |
| PunchToDeposit → RotateToTarget | Toggle | false | | Looks for a storage block nearby and aims at it by itself. |
| PunchToDeposit → Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autodeposit/ModuleAutoDeposit.kt)*
