## AutoCrafter

Automatically crafts items using the Recipe Book. Open a crafting table, furnace, smoker, blast furnace, or your inventory crafting grid, and AutoCrafter will repeatedly craft the items you have queued via the Recipe Book selection.

**Category:** Player
**Enabled by default:** No

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Delay (Integer Range | default: 2..3 | range: 1..20 | ticks)
├── StackCrafting (Toggle | default: true)
├── SequentialCrafting (Toggle | default: true)
├── OnFull (Choice | default: Wait | options: Disable, CloseScreen, Wait, Throw)
└── AllowedContainers (Multi-Select | default: CraftingTable | options: Inventory, CraftingTable, Furnace, BlastFurnace, Smoker)
```

### Settings Details

- **Delay** (Integer Range) — default: `2` – `3`; range: `1` – `20`; unit: ticks — Random delay between each crafting action.
- **StackCrafting** (Toggle) — default: `true` — Craft a full stack at once where the recipe allows it, instead of a single item per action.
- **SequentialCrafting** (Toggle) — default: `true` — Finish one recipe before starting the next instead of advancing through every queued item each tick.
- **OnFull** (Choice) — default: `Wait`; options: `Disable`, `CloseScreen`, `Wait`, `Throw` — What to do when there is no room for the crafted result: disable the module, close the screen, wait for space to free up, or throw the result on the ground.
- **AllowedContainers** (Multi-Select) — default: `CraftingTable`; options: `Inventory`, `CraftingTable`, `Furnace`, `BlastFurnace`, `Smoker` — Which crafting and smelting menus the module is allowed to operate in.

### Screenshots

*Screenshots for AutoCrafter will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleAutoCrafter.kt)*
