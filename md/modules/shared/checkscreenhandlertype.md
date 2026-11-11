## CheckScreenHandlerType

CheckScreenHandlerType decides in which kinds of containers a module works, like chests, double chests or shulker boxes. Turn the group off to let the module work in every container.

Used by: [AutoF5](/docs/modules/render/autof5), [AutoDeposit](/docs/modules/player/autodeposit), [ChestCleaner](/docs/modules/player/chestcleaner), [ChestStealer](/docs/modules/player/cheststealer).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| CheckScreenHandlerType | Toggleable Group | On | | Turns the check on or off. |
| Types | Registry List | Chest (3 rows), Chest (6 rows), Shulker Box | | The kinds of containers to check for. |
| Filter | Choice | Whitelist | Whitelist, Blacklist | Whitelist: only works in the listed containers. Blacklist: works everywhere except in the listed containers. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/inventory/InventoryValueGroups.kt)*
