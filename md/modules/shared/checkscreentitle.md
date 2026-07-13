## CheckScreenTitle

This shared group decides which open screens (containers like chests, barrels, and shulker boxes) a module is allowed to act on. Many container-handling features should only run when you actually have the right kind of inventory open — this group is how you tell them what counts as "the right kind."

It works by matching the title of the screen you currently have open. You pick a set of known container titles, optionally add your own custom entries, and then choose whether that list is a whitelist (only act on these) or a blacklist (act on everything except these). This lets you, for example, have a module trigger inside chests but ignore your crafting tables, furnaces, or special menus on certain servers.

Because servers often rename their GUIs, the custom list and the whitelist/blacklist switch give you the flexibility to fine-tune exactly where these modules kick in, instead of relying only on the default vanilla names.

This setting group is used by the following modules:
- [AutoF5](/docs/modules/render/autof5)
- [ChestCleaner](/docs/modules/player/chestcleaner)
- [ChestStealer](/docs/modules/player/cheststealer)

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Titles | Multi-Select | [Barrel, Chest, LargeChest, ShulkerBox, ChestMinecart, ChestBoat] | [Barrel, Beacon, BlastFurnace, BrewingStand, Chest, LargeChest, Dispenser, Dropper, EnderChest, Furnace, Hopper, ShulkerBox, Smoker, ChestMinecart, ChestBoat, HopperMinecart] | The list of known container screen types to match against. Pick which vanilla containers count for matching. The ChestBoat entry matches the titles of all chest boat and chest raft wood variants. |
| Custom | Editable List | — | — | Add your own screen titles here for servers that use renamed or non-vanilla GUIs, so they get matched too. |
| Filter | Choice | Whitelist | [Whitelist, Blacklist] | How the lists are applied. Whitelist means the module only acts on the listed screens; Blacklist means it acts on everything except the listed screens. |

---
*Last updated: 2026-07-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2)*
