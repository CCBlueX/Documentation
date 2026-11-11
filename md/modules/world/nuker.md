## Nuker

Nuker breaks the blocks around you by itself, one after another. Use it to clear land or dig out an area fast. Turn on [AutoTool](/docs/modules/world/autotool) too, so it always uses the right tool.

Legit mode looks at each block and mines it at normal speed, like a player would. Instant mode breaks many blocks every second, but servers notice that much more easily.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Legit | Legit, Instant | How blocks are broken. |
| Mode → [Legit] → Range | Decimal | 5.0 | 1.0..6.0 blocks | How far away blocks can be. |
| Mode → [Legit] → WallRange | Decimal | 0.0 | 0.0..6.0 blocks | How far it reaches through walls. 0 turns this off. It can't be more than Range. |
| Mode → [Legit] → ForceImmediateBreak | Toggle | false | | Tries to break each block at once instead of mining it slowly. |
| Mode → [Legit] → Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [Legit] → SwitchDelay | Integer | 0 | 0..20 ticks | How long to wait before moving to the next block, in ticks (20 per second). |
| Mode → [Instant] → Range | Decimal | 5.0 | 1.0..50.0 blocks | How far away blocks can be. |
| Mode → [Instant] → BPS | Integer Range | 40..50 | 1..200 | How many blocks it breaks per second. |
| Mode → [Instant] → DoNotStop | Toggle | false | | Doesn't tell the server that a block is done. Some servers break blocks faster this way. |
| AreaMode | Mode Selector | Sphere | Sphere, Floor | Sphere: breaks blocks all around you. Floor: breaks a box you set with two corners. |
| AreaMode → [Floor] → RelativeToPlayer | Toggle | true | | The corners move with you instead of staying at fixed coordinates. |
| AreaMode → [Floor] → StartPosition | Vector3_i | 0, 0, 0 | | One corner of the box (X, Y, Z). |
| AreaMode → [Floor] → EndPosition | Vector3_i | 0, 0, 0 | | The other corner of the box (X, Y, Z). |
| AreaMode → [Floor] → TopToBottom | Toggle | true | | Clears the top layer first and works down. |
| Filter | Choice | Blacklist | Whitelist, Blacklist | Whitelist: only break the listed blocks. Blacklist: break everything except the listed blocks. |
| Blocks | Registry List | | | The blocks the filter uses. |
| Swing | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Who sees your arm swing: everyone, nobody, only others, or only you. |
| IgnoreOpenInventory | Toggle | true | | Keeps breaking while a chest or your inventory is open. |
| TargetRendering | Toggleable Group | On | | Highlights the block being broken. See [Placement Rendering](/docs/modules/shared-settings/placement-rendering). |
| TargetRendering → ProgressText | Toggleable Group | On | | Shows how far the block is broken as text. |
| TargetRendering → ProgressText → Height | Decimal | 0.5 | -4.0..4.0 | How high above the block the text is. |
| TargetRendering → ProgressText → Scale | Decimal | 1.0 | 0.25..4.0 | Size of the text. |
| TargetRendering → ProgressText → Color | Color | White | | Color of the text. |
| TargetRendering → ProgressText → Shadow | Toggle | true | | Draws a shadow behind the text. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/nuker/ModuleNuker.kt)*
