## AutoCrafter

AutoCrafter turns your in-game Recipe Book into an automatic crafting machine. Open a crafting screen — your inventory's 2x2 grid, a crafting table, or even a furnace, blast furnace, or smoker — and the module will repeatedly craft any items you've listed for it, pulling the finished products out for you as it goes. It only works while the Recipe Book panel is actually open in that screen, so make sure the book is toggled on.

You tell it what to make with the **ItemsToCraft** list, and it only acts inside the container types you allow under **AllowedContainers**. It is smart about avoiding pointless loops: if one recipe in your list would consume an item that appears later in the same list (for example crafting a block back into ingots), it skips that recipe so you don't undo your own work. When a finished item can no longer fit in your inventory, the **OnFull** setting decides what happens — keep waiting, throw the extras out, close the screen, or simply turn off.

Use it for bulk crafting and smelting tasks where you'd otherwise be clicking the Recipe Book over and over: converting stone variants, mass-producing building blocks, or feeding ores into a furnace. Pair it with [InventoryCleaner](/docs/modules/player/inventorycleaner) if you want unwanted leftovers cleared out automatically.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| ItemsToCraft | Registry List | — | — | The items you want crafted. The module works through this list in order and only makes items it has a craftable recipe for. |
| Delay | Integer Range | 2..3 | 1..20 | How long to pause between crafting actions, in ticks. A random value in this range is picked each time to look less robotic. |
| StackCrafting | Toggle | true | — | When on, crafts a full stack at once where possible instead of one item per action, speeding up bulk jobs. |
| SequentialCrafting | Toggle | true | — | When on, only one craft is performed per cycle and the module waits before moving to the next item, instead of trying to craft everything in the list in a single pass. |
| OnFull | Choice | Wait | Disable, CloseScreen, Wait, Throw | What to do when a finished item can't fit in your inventory: Disable turns the module off, CloseScreen closes the crafting screen, Wait pauses until space frees up, and Throw drops the surplus item. |
| AllowedContainers | Multi-Select | CraftingTable | Inventory, CraftingTable, Furnace, BlastFurnace, Smoker | Which crafting and smelting screens the module is allowed to operate in. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoCrafter.kt)*
