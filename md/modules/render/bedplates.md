## BedPlates

BedPlates shows a small panel above each bed with the blocks that protect it and how far away the bed is. It is made for Bed Wars and similar modes, so you can see a bed's defense without walking around it.

Blocks you cannot break with the tools in your hotbar get a red count, so hard blocks like obsidian stand out. The closest beds are shown first.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Background | Mode Selector | Rect | Rect, Texture | The panel behind the icons. Rect is a rounded box, Texture uses item slot frames. |
| Background → [Rect] → Color | Color | | | Fill color of the box. |
| Background → [Rect] → OutlineColor | Color | | | Border color of the box. Clear by default. |
| Background → [Rect] → Margin | Decimal | 2.0 | 0.0..100.0 | Space between the icons and the edge of the box. |
| Background → [Rect] → Radius | Decimal | 4.0 | 0.0..16.0 | How round the corners are. |
| Background → [Rect] → Gradient | Decimal | 0.3 | 0.0..1.0 | How much darker the box gets toward the bottom. |
| Background → [Rect] → Glow | Decimal | 0.3 | 0.0..1.0 | Strength of the glow around the box. |
| Outline | Toggle | false | | Draws a border in the bed's color. |
| MaxLayers | Integer | 5 | 1..5 | How many layers of blocks around the bed are counted. |
| ShowBed | Toggle | true | | Shows the bed itself first, with its distance in meters. |
| TextShadow | Toggle | true | | Adds a shadow to the numbers so they are easier to read. |
| RenderOffset | Vector3_d | | | Moves the panel away from the bed. |
| Scale | Curve | 1 at every distance | Distance 0..200, Scale 0.25..4 | Panel size depending on how far away the bed is. |
| MaxCount | Integer | 8 | 1..64 | Most beds shown at once, closest first. |
| HighlightUnbreakable | Toggle | true | | Colors the count red for blocks you cannot break with your hotbar tools. |
| Compact | Toggle | true | | Adds up the same block from all layers into one icon. Off shows each layer separately. |
| PreventOverlap | Toggle | true | | Moves panels apart so they do not cover each other. |
| FilterMode | Mode Selector | Predefined | Predefined, Custom | Which blocks are listed. Predefined skips air and see-through blocks, but keeps glass, water and ladders. |
| FilterMode → [Custom] → Blocks | Registry List | | | Your own list of blocks. |
| FilterMode → [Custom] → Filter | Choice | Blacklist | Whitelist, Blacklist | Blacklist hides the listed blocks, Whitelist shows only them. |
| IgnoreSelfBed | Mode Selector | None | None, Color, SpawnLocation, Manual | How your own bed is found so it gets no panel. |
| IgnoreSelfBed → [Color] → Slots | Multi-Select | Head | Feet, Legs, Chest, Head | Armor pieces whose color is compared with the bed color. |
| IgnoreSelfBed → [Color] → Loose | Toggle | false | | Accepts colors that are only close to the bed color. |
| IgnoreSelfBed → [SpawnLocation] → BedDistance | Decimal | 24.0 | 16.0..48.0 | A bed this close to where you spawned counts as yours. |
| IgnoreSelfBed → [Manual] → Track | Key | Numpad + | | Marks the bed you look at as yours. |
| IgnoreSelfBed → [Manual] → Untrack | Key | Numpad - | | Removes that mark. |
| IgnoreAdjacent | Toggle | false | | Skips a bed when another bed is right next to it. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBedPlates.kt)*
