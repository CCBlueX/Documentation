## Scaffold

Scaffold places blocks under your feet while you walk, so you can bridge over gaps without looking down and clicking. Use it to cross the void in BedWars or to build a path quickly.

Technique sets how you bridge. Normal works for everyday bridging, GodBridge and Breezily are fast bridging styles, and Expand places a row of blocks in front of you. Pick a Tower mode and hold jump to build straight up. The Hypixel tower only works while you stand still and on the 1.8 protocol version, and it tells you in chat if one of these is wrong.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Delay | Integer Range | 0..0 | 0..40 ticks | Wait between blocks, in ticks (20 per second). |
| MinDist | Decimal | 0.0 | 0.0..0.25 | How far you must be from a block before it places a block on its side. |
| Timer | Decimal | 1.0 | 0.01..10.0 | Game speed while bridging. Above 1.0 is faster. |
| BlockItemSelection → Disallowed | Registry List | TNT, Cobweb, Nether Portal | | Blocks that are never placed. |
| BlockItemSelection → Unfavorable | Registry List | Crafting Table, Jigsaw, Smithing Table, Fletching Table, Enchanting Table, Cauldron, Magma Block | | Blocks only used when nothing else is left. |
| AutoBlock | Toggleable Group | On | | Picks a block from your hotbar for you. |
| AutoBlock → Always | Toggle | false | | Holds the block all the time, not only while placing. |
| AutoBlock → SlotResetDelay | Integer | 5 | 0..40 ticks | How long to wait before switching back to your old slot. |
| AutoBlock → DoNotUseBelowCount | Integer | 1 | 0..64 | Skips stacks with fewer blocks than this. |
| Prediction | Toggleable Group | On | | Aims at where you will stand when the block is placed, which makes bridging smoother. |
| Prediction → BootstrapBackoff | Decimal | 0.2 | 0.0..0.4 | How far behind the edge it aims before it has learned your speed. |
| Prediction → PredictionCutoffDistance | Decimal | 0.05 | 0.0..0.3 | How close to the edge you get before it stops aiming ahead. |
| Prediction → WarmupPlacements | Integer | 2 | 0..4 | How many blocks it places before it fully trusts what it learned. |
| Technique | Mode Selector | Normal | Normal, Expand, GodBridge, Breezily | How you bridge. |
| Technique → [Normal] → RotationMode | Choice | Stabilized | Center, Random, Stabilized, NearestRotation, ReverseYaw, DiagonalYaw, AngleYaw, EdgePoint | Where on the block you aim. |
| Technique → [Normal] → RequiresSight | Toggle | false | | Only places when you can really see the spot. |
| Technique → [Normal] → Eagle | Toggleable Group | Off | | Sneaks at the edge so you don't fall off. |
| Technique → [Normal] → Eagle → BlocksToEagle | Integer Range | 0..0 | 0..10 | How many blocks to place between sneaks. |
| Technique → [Normal] → Eagle → EdgeDistance | Decimal Range | 0.01..0.05 | 0.01..1.3 | How close to the edge you must be before it sneaks. |
| Technique → [Normal] → Eagle → OnlyOnGround | Toggle | true | | Only sneaks while you stand on the ground. |
| Technique → [Normal] → Telly | Toggleable Group | Off | | Jumps while you bridge, for faster "telly" bridging. |
| Technique → [Normal] → Telly → ResetMode | Choice | Reset | Reverse, Reset | How your view turns back between jumps. |
| Technique → [Normal] → Telly → Straight | Integer | 0 | 0..5 ticks | How long you walk straight before it starts. |
| Technique → [Normal] → Telly → Jump | Integer Range | 0..0 | 0..10 ticks | Wait before each jump. |
| Technique → [Normal] → Telly → AimOnTower | Toggle | true | | Keeps aiming at blocks while building up. |
| Technique → [Normal] → Down | Toggleable Group | Off | | Hold sneak to bridge downwards. |
| Technique → [Normal] → StabilizeMovement | Toggleable Group | On | | Keeps you in the middle of the bridge. |
| Technique → [Normal] → Ceiling | Toggleable Group | Off | | Places blocks above you instead of below. |
| Technique → [Normal] → HeadHitter | Toggleable Group | Off | | Jumps for you when there is a block above your head. |
| Technique → [Normal] → HeadHitter → JumpDelay | Integer Range | 0..0 | 0..20 ticks | Wait between jumps. |
| Technique → [Expand] → Length | Integer | 4 | 1..10 blocks | How far ahead it places blocks. |
| Technique → [GodBridge] → Modes | Multi-Select | Jump | Jump, Sneak, StopInput, Backwards | What it does at the edge so you don't fall. If a jump would take you two blocks high (with Jump Boost), it uses another mode or sneaks instead. |
| Technique → [GodBridge] → ForceSneakBelowCount | Integer | 3 | 0..10 | Sneaks instead when you have fewer blocks than this. |
| Technique → [GodBridge] → SneakTime | Integer Range | 1..1 | 1..10 | How long each sneak lasts. |
| Technique → [Breezily] → EdgeDistance | Decimal Range | 0.45..0.5 | 0.25..0.5 blocks | How far to the side it moves you. |
| SameY | Choice | Off | Off, On, JumpKey, Falling, Hypixel | Keeps the bridge at one height when you jump. JumpKey keeps the height unless you hold jump. |
| Tower | Mode Selector | None | None, Motion, Pulldown, Karhu-2024-05-10, Vulcan-2.8.8, Hypixel-2026-07-12 | How it builds up when you hold jump. |
| Tower → [Motion] → Motion | Decimal | 0.42 | 0.0..1.0 | How hard it pushes you up each step. |
| Tower → [Motion] → TriggerHeight | Decimal | 0.78 | 0.76..1.0 | How high you rise before the next push. |
| Tower → [Motion] → Slow | Decimal | 1.0 | 0.0..3.0 | How much your sideways speed is slowed. |
| Tower → [Pulldown] → Trigger | Decimal | 0.1 | 0.0..0.2 Y/v | Upward speed at which you get pulled down again. |
| Tower → [Karhu-2024-05-10] → Timer | Decimal | 5.0 | 0.1..10.0 | Game speed in this mode. |
| Tower → [Karhu-2024-05-10] → Trigger | Decimal | 0.06 | 0.0..0.2 Y/v | Upward speed at which you get pulled down again. |
| Tower → [Karhu-2024-05-10] → Pulldown | Toggle | true | | Pulls you down after each step. |
| SafeWalk | Mode Selector | Safe | None, Safe, OnEdge | Stops you from walking off edges. |
| SafeWalk → [OnEdge] → Distance | Decimal Range | 0.1..0.15 | 0.05..0.5 | How close to the edge it reacts. |
| SafeWalk → [OnEdge] → Keep | Integer Range | 1..2 | 1..20 ticks | How long it keeps reacting. |
| SafeWalk → [OnEdge] → Mode | Choice | Stop | Stop, Invert, Center | Stop: you stop. Invert: you move back. Center: you move to the middle of the block. |
| SafeWalk → [OnEdge] → Sneak | Integer Range | 0..0 | 0..20 ticks | How long to sneak at the edge. |
| SafeWalk → [OnEdge] → Jump | Toggle | false | | Lets it jump at the edge. |
| Swing | Choice | DoNotHide | DoNotHide, HideForClient | Whether you see your arm swing. |
| Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |
| Rotations → ConsiderInventory | Toggle | false | | Doesn't turn your view while your inventory is open. |
| Rotations → RotationTiming | Choice | Normal | Normal, OnTick, OnTickSnap | Normal: turns before placing. OnTick: turns at the moment of placing. OnTickSnap: like OnTick, but keeps the view after placing. |
| SprintControl | Toggleable Group | Off | | Changes sprinting while you bridge. |
| SprintControl → Client | Choice | DoNotChange | DoNotChange, ForceSprint, ForceNoSprint, NoSprintOnPlace, NoSprintOnGround | Sprinting as you see it. |
| SprintControl → Server | Choice | DoNotChange | DoNotChange, ForceSprint, ForceNoSprint, NoSprintOnPlace, NoSprintOnGround | Sprinting as the server sees it. |
| SimulatePlacementAttempts | Toggleable Group | Off | | Clicks like a real player who tries to place blocks, even when there is nothing to place. |
| SimulatePlacementAttempts → Clicker | Setting Group | | | See [Clicker](/docs/modules/shared-settings/clicker). |
| SimulatePlacementAttempts → FailedAttemptsOnly | Toggle | true | | Only makes clicks that don't place a block. |
| Acceleration | Toggleable Group | Off | | Changes your walking speed while you bridge. |
| Acceleration → SpeedMultiplier | Decimal | 0.6 | 0.1..3.0 | How much your speed is multiplied by. |
| Acceleration → OnlyOnGround | Toggle | false | | Only changes speed on the ground. |
| Strafe | Toggleable Group | Off | | Keeps your speed the same while you bridge. |
| Strafe → Speed | Decimal | 0.247 | 0.0..5.0 | The speed to keep. |
| Strafe → Hypixel | Toggle | false | | Uses speeds made for Hypixel. |
| Strafe → OnlyOnGround | Toggle | false | | Only works on the ground. |
| StrafeOnJump | Toggleable Group | Off | | Gives you a speed boost when you jump. |
| StrafeOnJump → StraightSpeed | Decimal Range | 0.48..0.49 | 0.1..1.0 | Boost when you walk straight. |
| StrafeOnJump → DiagonalSpeed | Decimal Range | 0.48..0.49 | 0.1..1.0 | Boost when you walk diagonally. |
| SpeedLimiter | Toggleable Group | Off | | Slows you down when you get too fast. |
| SpeedLimiter → SpeedLimit | Decimal | 0.11 | 0.01..0.4 | The highest speed allowed. |
| Blink | Toggleable Group | Off | | Holds back what you send to the server for a moment after each block. |
| Blink → Time | Integer Range | 50..250 | 0..3000 ms | How long to hold back. |
| Blink → FlushOn | Multi-Select | None | Place, Towering, Sneaking, NotSneaking, OnGround, InAir | When to send everything at once. |
| AutoSpeed | Toggle | false | | Turns on [Speed](/docs/modules/movement/speed) while Scaffold is on. |
| Ledge | Toggle | true | | Jumps or sneaks at edges so you don't fall. |
| Render | Toggleable Group | On | | See [Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/scaffold/ModuleScaffold.kt)*
