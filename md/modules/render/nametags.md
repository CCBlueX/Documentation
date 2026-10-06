## Nametags

Nametags replaces Minecraft's default name tags with a richer, more readable overlay. Instead of the vanilla floating label, each nearby player (and other living entities) gets a customisable tag showing any combination of their name, current health, ping, distance, game mode, and whether they have been flagged as a bot by [AntiBot](/docs/modules/misc/antibot). The tag scales smoothly with distance according to a configurable curve, so it stays readable up close without overwhelming the screen at range, and vanilla name tags are suppressed while the module is active.

Above the text tag, Nametags can also display a row of item icons representing the equipment each entity is wearing or holding. Enchantments on those items are summarised as short abbreviations (e.g. "Sha5", "Pro4") rendered in colour-coded badges directly above the item icon — curses appear in red, high-level enchantments in gold or yellow. If an entity is actively using an item (drawing a bow, eating, etc.) that item's slot can be highlighted with a configurable fill and outline colour so you can tell at a glance what they are doing.

Use this module in PvP scenarios, on practice servers, or any time you want at-a-glance combat information about the players around you. It pairs naturally with [ESP](/docs/modules/render/esp) and [Tracers](/docs/modules/render/tracers) for a complete awareness setup.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Text → Parts | Multi-Select | Distance, Ping, Name, Health, BotMark | Distance, Ping, Name, Health, GameMode, BotMark | Choose which pieces of information appear in the name tag text. |
| Equipment → Slots | Multi-Select | Mainhand, Head, Chest, Legs, Feet, Offhand | Mainhand, Offhand, Feet, Legs, Chest, Head, Body, Saddle | Which equipment slots are shown as item icons above the name tag. |
| Equipment → SkipEmptySlot | Toggle | true | — | When enabled, slots that contain no item are hidden instead of showing a blank space. |
| Equipment → ShowInfo | Toggle | true | — | When enabled, item tooltips (durability, count, etc.) are shown alongside the item icons. |
| Equipment → Enchantment | Toggleable Group | on | — | Shows abbreviated enchantment labels above each item icon. |
| Equipment → Enchantment → Scale | Decimal | 0.8 | 0.25–4.0 | Size of the enchantment label text relative to the default font size. |
| Equipment → Enchantment → MaxCountPerItem | Integer | 4 | 1–16 | Maximum number of enchantment badges displayed per item; additional enchantments are replaced with "…". |
| Equipment → Enchantment → BackgroundRadius | Decimal | 1.0 | 0.0–8.0 | Corner rounding radius of the enchantment label background pill. |
| Equipment → HighlightItemInUse | Toggleable Group | off | — | Draws a coloured overlay on the item slot of whatever item the entity is currently using. |
| Equipment → HighlightItemInUse → FillColor | Color | — | — | Fill colour of the in-use item highlight overlay. |
| Equipment → HighlightItemInUse → OutlineColor | Color | — | — | Outline colour of the in-use item highlight overlay. |
| BorderWidth | Decimal | 1.0 | 0.0–8.0 | Thickness of the border drawn around the name tag background. |
| BackgroundRadius | Decimal | 2.0 | 0.0–16.0 | Corner rounding radius of the name tag background. |
| Scale | Curve | — | — | Distance-to-scale curve controlling how large the name tag appears at different distances (x-axis: distance 0–200, y-axis: scale 0.25–4). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/nametags/ModuleNametags.kt)*
