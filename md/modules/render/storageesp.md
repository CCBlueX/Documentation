## StorageESP

StorageESP highlights storage containers — chests, barrels, ender chests, furnaces, brewing stands, hoppers, shulker boxes, decorated pots, shelves, and more — through solid terrain so you can spot loot and resources at a glance. The module scans chunks as they load and also tracks container entities in the world, including chest minecarts, chest boats, and pack horses.

Two rendering modes are available. **Box** mode draws a semi-transparent coloured box over every matched storage block and, when **Outline** is on, adds a crisp border around it. **Glow** mode uses Minecraft's built-in outline glow effect for a subtler look that blends more naturally with the game's visuals. Every storage type has its own configurable colour and an optional **Tracers** toggle that draws a beam from your crosshair to each block, making distant containers easy to locate even in large caves or bases.

You can narrow the module's scope with **RequiresChestStealer**, which suppresses all highlights unless [ChestStealer](/docs/modules/player/cheststealer) is also running — handy when you only want the overlay during automated looting. Enabling **MergeAdjacent** fuses the rendered outlines of neighbouring storage blocks into one combined shape, reducing visual noise in areas densely packed with chests.

**Category:** Render  
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Glow | Box, Glow | Controls how storage blocks are highlighted. **Box** draws a coloured bounding box; **Glow** uses Minecraft's glow outline effect. |
| Mode → [Box] → Outline | Toggle | true | — | When enabled, draws an outline border around the coloured box faces. |
| Chest | Toggleable Group | on | — | Highlight settings for chests, including chest minecarts, chest boats, and horses carrying a chest. |
| Chest → Color | Color | — | — | Highlight colour for chests. |
| Chest → Tracers | Toggle | false | — | Draws a line from your crosshair to each visible chest. |
| Barrel | Toggleable Group | on | — | Highlight settings for barrels. |
| Barrel → Color | Color | — | — | Highlight colour for barrels. |
| Barrel → Tracers | Toggle | false | — | Draws a line from your crosshair to each visible barrel. |
| EnderChest | Toggleable Group | on | — | Highlight settings for ender chests. |
| EnderChest → Color | Color | — | — | Highlight colour for ender chests. |
| EnderChest → Tracers | Toggle | false | — | Draws a line from your crosshair to each visible ender chest. |
| Furnace | Toggleable Group | on | — | Highlight settings for furnaces, blast furnaces, and smokers. |
| Furnace → Color | Color | — | — | Highlight colour for furnaces. |
| Furnace → Tracers | Toggle | false | — | Draws a line from your crosshair to each visible furnace. |
| BrewingStand | Toggleable Group | on | — | Highlight settings for brewing stands. |
| BrewingStand → Color | Color | — | — | Highlight colour for brewing stands. |
| BrewingStand → Tracers | Toggle | false | — | Draws a line from your crosshair to each visible brewing stand. |
| Dispenser | Toggleable Group | on | — | Highlight settings for dispensers, droppers, and crafter blocks. |
| Dispenser → Color | Color | — | — | Highlight colour for dispensers. |
| Dispenser → Tracers | Toggle | false | — | Draws a line from your crosshair to each visible dispenser. |
| Hopper | Toggleable Group | on | — | Highlight settings for hoppers and hopper minecarts. |
| Hopper → Color | Color | — | — | Highlight colour for hoppers. |
| Hopper → Tracers | Toggle | false | — | Draws a line from your crosshair to each visible hopper. |
| ShulkerBox | Toggleable Group | on | — | Highlight settings for shulker boxes. |
| ShulkerBox → Color | Color | — | — | Highlight colour for shulker boxes. |
| ShulkerBox → Tracers | Toggle | false | — | Draws a line from your crosshair to each visible shulker box. |
| Pot | Toggleable Group | on | — | Highlight settings for decorated pots. |
| Pot → Color | Color | — | — | Highlight colour for decorated pots. |
| Pot → Tracers | Toggle | false | — | Draws a line from your crosshair to each visible decorated pot. |
| Shelf | Toggleable Group | on | — | Highlight settings for shelves. |
| Shelf → Color | Color | — | — | Highlight colour for shelves. |
| Shelf → Tracers | Toggle | false | — | Draws a line from your crosshair to each visible shelf. |
| RequiresChestStealer | Toggle | false | — | When enabled, the module's highlights are only shown while [ChestStealer](/docs/modules/player/cheststealer) is also active. |
| MergeAdjacent | Toggle | false | — | Merges the outlines of directly adjacent storage blocks into a single combined shape, reducing visual clutter in densely packed areas. |
| DistanceFade | Setting Group | — | — | See [Shared: DistanceFade](/docs/modules/shared-settings/distancefade). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleStorageESP.kt)*
