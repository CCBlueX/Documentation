## Nametags

Nametags replaces the normal name tags above players and mobs with bigger, easier to read ones. A tag can show the name, health, ping, distance, game mode, and a mark if [AntiBot](/docs/modules/misc/antibot) thinks the player is a bot. The normal Minecraft name tags are hidden while it is on.

Above the tag you can see the armor and items each player has, with short names for their enchantments. Curses are shown in red. If a player is using an item, like eating or drawing a bow, that item can be highlighted.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Text → Parts | Multi-Select | Distance, Ping, Name, Health, GameMode, BotMark | Distance, Ping, Name, Health, GameMode, BotMark | What the tag shows. At least one must be picked. |
| Equipment → Slots | Multi-Select | Mainhand, Head, Chest, Legs, Feet, Offhand | Mainhand, Offhand, Feet, Legs, Chest, Head, Body, Saddle | Which items and armor are shown above the tag. |
| Equipment → SkipEmptySlot | Toggle | true | | Leaves out empty slots instead of showing a gap. |
| Equipment → ShowInfo | Toggle | true | | Shows the stack count and durability on each item. |
| Equipment → Enchantment | Toggleable Group | On | | Shows short enchantment names above each item. |
| Equipment → Enchantment → Scale | Decimal | 0.8 | 0.25 to 4.0 | Size of the enchantment text. |
| Equipment → Enchantment → MaxCountPerItem | Integer | 4 | 1 to 16 | How many enchantments are shown per item at most. |
| Equipment → Enchantment → BackgroundRadius | Decimal | 1.0 | 0.0 to 8.0 | How round the corners behind the enchantment text are. |
| Equipment → Enchantment → Enchantments | Registry List | Empty | | The enchantments used by Filter. |
| Equipment → Enchantment → Filter | Choice | Blacklist | Whitelist, Blacklist | Whether the Enchantments list picks the enchantments to show or the ones to hide. |
| Equipment → HighlightItemInUse | Toggleable Group | Off | | Highlights the item a player is using right now. |
| Equipment → HighlightItemInUse → FillColor | Color | Red, alpha 100 | | Fill color of the highlight. |
| Equipment → HighlightItemInUse → OutlineColor | Color | Transparent | | Outline color of the highlight. |
| BorderWidth | Decimal | 1.0 | 0.0 to 8.0 | How thick the border around the tag is. |
| BackgroundRadius | Decimal | 2.0 | 0.0 to 16.0 | How round the tag's corners are. |
| Scale | Curve | 1 at every distance | Distance 0 to 200, Scale 0.25 to 4 | How big the tag is at each distance. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/nametags/ModuleNametags.kt)*
