## AutoFarm

AutoFarm does the tedious work of harvesting and replanting for you. When enabled, it scans nearby blocks for fully grown crops — wheat, carrots, potatoes, beetroot, nether wart, cocoa, melons, pumpkins, sugar cane, cactus, bamboo, kelp and sweet berries — aims at them, and harvests each one automatically. It also replants seeds on empty farmland and soul sand, and can apply bone meal to speed crops along, so a field can keep producing with little input from you.

It works best when you stand within reach of your crops, but it can also walk between targets and pick up dropped produce when the AutoWalk group is turned on. You can cap things so it stops once your inventory fills up, and there are built-in visuals that highlight ready, plantable and currently targeted blocks so you can see exactly what it's doing.

Note that AutoFarm pauses while you have a container open (like a chest or your inventory) and while [Blink](/docs/modules/player/blink) is active, so it won't interfere with those.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 5.0 | 1.0..6.0 | How far away (in blocks) crops can be to be harvested or planted. |
| WallRange | Decimal | 0.0 | 0.0..6.0 | How far it may reach for targets that are behind walls or otherwise out of direct line of sight. Capped at Range. |
| InteractDelay | Integer Range | 2..3 | 1..15 | Ticks to wait after each interaction. A random value in this range is picked each time for more natural pacing. |
| DisableOnFullInventory | Toggle | false | — | Turns AutoFarm off and shows a notification when your inventory has no free space. |
| UseFortune | Toggle | true | — | Silently switches to a Fortune-enchanted tool before breaking crops to increase drops. |
| AutoWalk | Toggleable Group | Off | — | See [Shared: AutoWalk](/docs/modules/shared-settings/autowalk). |
| AutoPlant | Toggleable Group | On | — | Replants seeds, nether wart and cocoa on empty farmland, soul sand and jungle logs. |
| AutoPlant → SwapBackDelay | Integer Range | 1..2 | 1..20 | Ticks to wait before switching back from the seed slot after planting. |
| AutoUseBoneMeal | Toggleable Group | Off | — | Applies bone meal from your hotbar or offhand to nearby crops that can still grow. |
| AutoUseBoneMeal → UseDelay | Integer Range | 20..200 | 0..20000 | Delay (in milliseconds) between bone meal uses, randomized within the range. |
| AutoUseBoneMeal → SwapBackDelay | Integer Range | 1..2 | 1..20 | Ticks to wait before switching back from the bone meal slot after use. |
| Visualize | Toggleable Group | On | — | Master toggle for AutoFarm's on-screen highlights. |
| Visualize → Path | Toggleable Group | On | — | Draws a line to the block AutoWalk is heading toward. |
| Visualize → Path → PathColor | Color | — | — | Color of the walk path line. |
| Visualize → Blocks | Toggleable Group | On | — | Highlights tracked crops and plantable spots in the world. |
| Visualize → Blocks → Outline | Toggle | true | — | Draws an outline around highlighted blocks. |
| Visualize → Blocks → ReadyColor | Color | — | — | Color used for blocks that are ready to harvest. |
| Visualize → Blocks → PlaceColor | Color | — | — | Color used for spots where crops can be planted. |
| Visualize → Blocks → Range | Integer | 50 | 10..128 | How far (in blocks) the highlights are drawn around you. |
| Visualize → Blocks → Rainbow | Toggle | false | — | Cycles the highlight colors through a rainbow instead of the set colors. |
| Visualize → Blocks → PlaceTargets | Multi-Select | [Farmland, SoulSand, JungleLogs] | [Farmland, SoulSand, JungleLogs] | Which plantable surfaces to highlight. |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/autofarm/ModuleAutoFarm.kt)*
