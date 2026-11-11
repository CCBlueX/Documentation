## AutoFarm

AutoFarm harvests grown crops near you and plants new seeds. It works with wheat, carrots, potatoes, beetroot, nether wart, cocoa, melons, pumpkins, sugar cane, cactus, bamboo, kelp and sweet berries. It can also use bone meal and walk to your crops and pick up the drops.

It pauses while a chest or your inventory is open.

<video src="/images/modules/autofarm/autofarm-walk.mp4" controls width="600">Your browser does not support the video tag.</video>

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 5.0 | 1.0..6.0 blocks | How far away crops can be. |
| WallRange | Decimal | 0.0 | 0.0..6.0 blocks | How far it can reach crops behind blocks. Never more than Range. |
| InteractDelay | Integer Range | 2..3 | 1..15 ticks | Wait after each harvest or plant (20 ticks per second). |
| UseFortune | Toggle | true | | Switches to a Fortune tool to get more drops. |
| DisableOnFullInventory | Toggle | false | | Turns AutoFarm off when your inventory is full. |
| AutoPlant | Toggleable Group | On | | Plants seeds on empty farmland, nether wart on soul sand and cocoa on jungle logs. |
| AutoPlant → SwapBackDelay | Integer Range | 1..2 | 1..20 ticks | Wait before switching back to your old item. |
| AutoUseBoneMeal | Toggleable Group | Off | | Uses bone meal on crops that are still growing. |
| AutoUseBoneMeal → UseDelay | Integer Range | 20..200 | 0..20000 ms | Wait between bone meal uses. |
| AutoUseBoneMeal → SwapBackDelay | Integer Range | 1..2 | 1..20 ticks | Wait before switching back to your old item. |
| Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |
| AutoWalk | Toggleable Group | On | | Walks to crops and items when nothing is in reach. See [AutoWalk](/docs/modules/shared-settings/autowalk). |
| AutoWalk → ToPlant | Toggle | true | | Also walks to spots where it can plant. |
| AutoWalk → ToItems | Toggleable Group | On | | Walks over dropped items to pick them up. |
| AutoWalk → ToItems → Range | Decimal | 20.0 | 8.0..64.0 blocks | How far away items can be. |
| AutoWalk → ToItems → Items | Registry List | | | Items the filter uses. |
| AutoWalk → ToItems → Filter | Choice | Blacklist | Whitelist, Blacklist | Whitelist picks up only the listed items. Blacklist picks up everything else. |
| BlockESP | Toggleable Group | On | | Highlights crops and planting spots. |
| BlockESP → Outline | Toggle | true | | Draws an outline around the blocks. |
| BlockESP → ReadyColor | Color | | | Color of crops ready to harvest. |
| BlockESP → PlaceColor | Color | | | Color of spots where it can plant. |
| BlockESP → Range | Integer | 50 | 10..128 blocks | How far away blocks get highlighted. |
| BlockESP → Rainbow | Toggle | false | | Uses rainbow colors. |
| BlockESP → PlaceTargets | Multi-Select | Farmland, SoulSand, JungleLogs | Farmland, SoulSand, JungleLogs | Which planting spots to highlight. |
| BlockESP → CurrentTarget | Toggleable Group | On | | Highlights the block it is working on. |
| BlockESP → CurrentTarget → Color | Color | | | Color of that block. |
| BlockESP → CurrentTarget → Rainbow | Toggle | false | | Uses rainbow colors. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/autofarm/ModuleAutoFarm.kt)*
