## CheckScreenTitle

CheckScreenTitle decides in which containers a module works, by looking at the name at the top of the open container. Many servers use chest menus for things like shops. Since those menus often have other names, this keeps the module out of them. Turn the group off to let the module work in every container.

Used by: [AutoF5](/docs/modules/render/autof5), [AutoDeposit](/docs/modules/player/autodeposit), [ChestCleaner](/docs/modules/player/chestcleaner), [ChestStealer](/docs/modules/player/cheststealer).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| CheckScreenTitle | Toggleable Group | On | | Turns the check on or off. |
| Titles | Multi-Select | Barrel, Chest, LargeChest, ShulkerBox, ChestMinecart, ChestBoat | Barrel, Beacon, BlastFurnace, BrewingStand, Chest, LargeChest, Dispenser, Dropper, EnderChest, Furnace, Hopper, ShulkerBox, Smoker, ChestMinecart, ChestBoat, HopperMinecart | Normal Minecraft container names to look for. ChestBoat counts all kinds of chest boats and rafts. |
| Custom | Text List | | | More names to look for, for example a server's own menu names. |
| Filter | Choice | Whitelist | Whitelist, Blacklist | Whitelist: only works in containers with these names. Blacklist: works everywhere except in containers with these names. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/inventory/InventoryValueGroups.kt)*
