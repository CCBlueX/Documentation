## AutoDeposit

AutoDeposit is the counterpart to [ChestStealer](/docs/modules/player/cheststealer): instead of pulling loot out of a container, it pushes items out of your inventory into whatever container you have open. Open a chest, barrel or shulker box and every stack matching your filter is quick-moved across, which makes it ideal for emptying a full inventory into a storage room or dumping junk blocks while building.

Use the **Filter** setting to decide how the **Items** list is read: in Whitelist mode only the listed items are deposited, in Blacklist mode everything *except* them is. Stacks the container can no longer absorb are left alone rather than clicked forever, and with **AutoClose** the screen closes by itself once there is nothing left to move — but only for containers it actually deposited into, so manually opened chests stay open.

**PunchToDeposit** adds a hands-free variant: punch a storage block and the first matching stack from your hotbar is deposited without the container GUI ever opening. It can look for a block on its own with **RotateToTarget**, and pauses while you are in combat or using an item if you select those conditions.

**Category:** Player
**Enabled by default:** No
**Aliases:** AutoStore, ContainerStorer

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Filter | Choice | Whitelist | Whitelist, Blacklist | Whether the Items list is treated as a whitelist (only listed items are deposited) or a blacklist (everything except listed items is deposited). |
| Items | Registry List | — | — | The items this module looks for, interpreted according to the Filter mode. |
| AutoClose | Toggle | true | — | Closes the container automatically once there is nothing left to deposit. Only applies to containers the module has deposited into. |
| Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| CheckScreenHandlerType | Toggleable Group | on | — | See [Shared: CheckScreenHandlerType](/docs/modules/shared-settings/checkscreenhandlertype). |
| CheckScreenTitle | Toggleable Group | on | — | See [Shared: CheckScreenTitle](/docs/modules/shared-settings/checkscreentitle). |
| PunchToDeposit | Toggleable Group | Off | — | Lets you punch a storage block to deposit a stack from your hotbar without opening it. |
| PunchToDeposit → Range | Decimal | 3.0 | 1.0–6.0 | How far away (in blocks) a storage block can be for you to punch it. |
| PunchToDeposit → WallRange | Decimal | 0.0 | 0.0–6.0 | Reach for storage blocks you don't have line of sight to; capped at the Range value. |
| PunchToDeposit → Delay | Integer | 5 | 1–80 ticks | Wait time between one punch and the next. |
| PunchToDeposit → SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Whether and where the hand-swing animation is shown when punching a block. |
| PunchToDeposit → PauseOn | Multi-Select | None | Combat, UsingItem | Conditions that temporarily halt depositing by punch. |
| PunchToDeposit → ValidStorageBlocks | Registry List | Chest, EnderChest | — | Which block types count as storage and can be punched. |
| PunchToDeposit → RotateToTarget | Toggle | false | — | Searches for a nearby storage block and aims at it instead of only using the block you are already looking at. |
| PunchToDeposit → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-09-19*
