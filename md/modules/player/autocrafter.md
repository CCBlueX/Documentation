## AutoCrafter

AutoCrafter crafts the items on your list again and again and takes them out for you. It uses the recipe book, so open a crafting screen and make sure the recipe book is open. It also works in furnaces, blast furnaces and smokers.

Use it when you need a lot of one thing, like building blocks or smelted ores. It skips a recipe that would use up an item further down your list, so it won't undo its own work (for example turning blocks back into ingots).

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| ItemsToCraft | Registry List | Polished Deepslate, Deepslate Bricks, Deepslate Tiles | | Items to craft, in this order. |
| Delay | Integer Range | 2..3 | 1..20 ticks | Wait between crafts, in ticks (20 per second). |
| StackCrafting | Toggle | true | | Crafts a whole stack at once when it can. |
| SequentialCrafting | Toggle | true | | Crafts one item from the list each round instead of going through the whole list at once. |
| OnFull | Choice | Wait | Disable, CloseScreen, Wait, Throw | What to do when your inventory is full: turn the module off, close the screen, wait for space, or throw the item away. |
| AllowedContainers | Multi-Select | CraftingTable | Inventory, CraftingTable, Furnace, BlastFurnace, Smoker | Screens where it is allowed to craft. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoCrafter.kt)*
