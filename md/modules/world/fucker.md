## Fucker

Fucker breaks certain blocks near you by itself. In BedWars it breaks enemy beds for you. By default it goes after all beds and dragon eggs, and you can add any other block.

Use SelfBed so it leaves your own bed alone. If the bed is covered, Entrance and Surroundings let it break the blocks in the way first. With AutoWalk on, it walks to the closest bed that is out of reach.

<video src="/images/modules/fucker/fucker-walk.mp4" controls width="600">Your browser does not support the video tag.</video>

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 5.0 | 1.0..6.0 blocks | How far away a block you can see may be. |
| WallRange | Decimal | 0.0 | 0.0..6.0 blocks | How far away a block behind a wall may be. 0 turns this off. It can't be more than Range. |
| Entrance | Toggleable Group | Off | | Breaks a target that has any open side, even if you can't see it. |
| Entrance → BreakFree | Toggle | true | | If no side is open, breaks the weakest block next to the target first. |
| Surroundings | Toggle | true | | Breaks the blocks that cover a target so it can get to it. |
| Targets | Registry List | All beds, Dragon Egg | | The blocks it goes after. |
| Delay | Integer | 0 | 0..20 ticks | How long to wait between targets, in ticks (20 per second). |
| Action | Choice | Destroy | Destroy, Use | Destroy breaks the block. Use right-clicks it. |
| SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Who sees your arm swing: everyone, nobody, only others, or only you. |
| ForceImmediateBreak | Toggle | false | | Tries to break the block at once instead of mining it slowly. |
| IgnoreOpenInventory | Toggle | true | | Keeps working while a chest or your inventory is open. |
| IgnoreUsingItem | Toggle | true | | Keeps working while you eat, drink or use a bow. |
| NotDuringCombat | Toggle | false | | Stops while you are fighting. |
| PrioritizeOverKillAura | Toggle | false | | Lets Fucker aim before [KillAura](/docs/modules/combat/killaura) does. |
| ChestAsFullBlock | Toggle | false | | Treats chests like a full block. |
| SelfBed | Mode Selector | None | None, Color, SpawnLocation, Manual | How it finds your own bed so it doesn't break it. None protects no bed. |
| SelfBed → [Color] → Slots | Multi-Select | Head | Feet, Legs, Chest, Head | Which armor pieces are checked. A bed with the same color as your armor is yours. |
| SelfBed → [Color] → Loose | Toggle | false | | Also counts beds with a color close to your armor color. |
| SelfBed → [SpawnLocation] → BedDistance | Decimal | 24.0 | 16.0..48.0 blocks | A bed this close to where you spawned is yours. |
| SelfBed → [Manual] → Track | Key | Numpad + | | Marks a bed as yours. |
| SelfBed → [Manual] → Untrack | Key | Numpad - | | Removes the mark again. |
| Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |
| TargetRendering | Toggleable Group | On | | Highlights the target block. See [Placement Rendering](/docs/modules/shared-settings/placement-rendering). |
| TargetRendering → ProgressText | Toggleable Group | On | | Shows how far the block is broken as text. |
| TargetRendering → ProgressText → Height | Decimal | 0.5 | -4.0..4.0 | How high above the block the text is. |
| TargetRendering → ProgressText → Scale | Decimal | 1.0 | 0.25..4.0 | Size of the text. |
| TargetRendering → ProgressText → Color | Color | White | | Color of the text. |
| TargetRendering → ProgressText → Shadow | Toggle | true | | Draws a shadow behind the text. |
| AutoWalk | Toggleable Group | Off | | Walks to the closest target when none is in reach. It can bridge, build up and dig on the way. See [AutoWalk](/docs/modules/shared-settings/autowalk). |
| AutoWalk → TargetRange | Decimal | 64.0 | 8.0..256.0 blocks | How far away a target can be to walk to it. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/fucker/ModuleFucker.kt)*
