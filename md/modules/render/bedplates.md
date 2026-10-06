## BedPlates

BedPlates draws a floating overlay over every bed it can find in your view distance, showing you exactly which blocks are protecting it. This is built for bed-defense game modes (Bedwars and similar): instead of flying around each bed to inspect its defense, you get an at-a-glance icon strip of the surrounding blocks, each with a stacked count, plus the bed's distance in meters. Beds are scanned asynchronously and the overlays are sorted by distance so the closest beds render first.

For each bed, the mod collects the surrounding blocks, filters them, and turns them into a list of item icons. By default it uses **Compact** mode (merging blocks of the same type across layers into one count) and **ShowBed** (the bed itself appears first in the strip with its distance label). Blocks you can't currently break — those that need a tool you don't have in your hotbar — are highlighted in red so you can spot reinforced defenses like obsidian or end stone; see [the unbreakable-block check](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBedPlates.kt#L230-L237). The full per-bed gather, filter, and sort pass lives in [updateAndSortBeds](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBedPlates.kt#L145-L168).

To cut clutter, you can limit how many beds are shown at once, scale the overlay by distance, filter which blocks are listed, and tell the mod to skip your own bed. The skip logic (own bed and adjacent beds) and distance scaling are applied at [render time](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBedPlates.kt#L199-L208).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| BackgroundColor | Color | — | — | Color of the rectangular background drawn behind each bed's icon strip. |
| Outline | Toggle | false | — | Draws an outline around the overlay using the bed's wool color. When off, no outline is drawn. |
| MaxLayers | Integer | 5 | 1..5 | How many block layers outward from the bed to scan and display. Changing it triggers a full rescan. |
| ShowBed | Toggle | true | — | Includes the bed itself as the first icon in the strip, labeled with the bed's distance in meters. |
| TextShadow | Toggle | true | — | Renders a drop shadow behind the count and layer text for readability. |
| RenderOffset | Vector3_d | — | — | World-space offset applied to the bed position before projecting it to the screen, nudging the overlay's location. |
| Scale | Curve | — | — | Maps camera distance (0–200) to an overlay scale (0.25–4). Lets distant beds shrink or stay readable; overlays below 0.01 scale are skipped. |
| MaxCount | Integer | 8 | 1..64 | Maximum number of beds rendered at once, starting with the closest. |
| HighlightUnbreakable | Toggle | true | — | Colors a block's count red when it requires a tool you don't currently have in your hotbar to break. |
| Compact | Toggle | true | — | Merges identical surrounding blocks across layers into a single counted icon. When off, each layer is shown separately with a Roman-numeral layer label. |
| PreventOverlap | Toggle | true | — | Prevents bed overlays from drawing on top of each other when beds are close together on screen. |
| FilterMode | Mode Selector | Predefined | Predefined, Custom | Chooses how surrounding blocks are filtered. Predefined hides air and non-solid blocks (except a built-in whitelist like glass, water, and ladders); Custom uses your own block list. |
| FilterMode → [Custom] → Blocks | Registry List | — | — | The list of blocks used by the Custom filter. |
| FilterMode → [Custom] → Filter | Choice | Blacklist | Whitelist, Blacklist | Whether the Blocks list is treated as a blacklist (hide listed blocks) or whitelist (show only listed blocks). |
| IgnoreSelfBed | Mode Selector | None | None, Color, SpawnLocation, Manual | How to detect and skip your own bed so its plate isn't drawn. None disables this. |
| IgnoreSelfBed → [Color] → Slots | Multi-Select | Head | Feet, Legs, Chest, Head | Armor slots whose color is compared against bed colors to identify your team's bed. |
| IgnoreSelfBed → [Color] → Loose | Toggle | false | — | Loosens the color match used to identify your own bed. |
| IgnoreSelfBed → [SpawnLocation] → BedDistance | Decimal | 24.0 | 16.0..48.0 | Maximum distance from your spawn point within which a bed is treated as your own. |
| IgnoreSelfBed → [Manual] → Track | Key | — | — | Key to manually mark the bed you're looking at as your own (to be ignored). |
| IgnoreSelfBed → [Manual] → Untrack | Key | — | — | Key to remove a manual self-bed mark. |
| IgnoreAdjacent | Toggle | false | — | Skips a bed's overlay when another tracked bed sits directly adjacent to it, avoiding duplicate plates for double beds. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleBedPlates.kt)*
