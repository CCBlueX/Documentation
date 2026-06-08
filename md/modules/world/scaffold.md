## Scaffold

Scaffold automatically bridges for you. As you walk forward over a gap, it places blocks into the empty space beneath your feet so you can keep moving without manually aiming down and clicking. It's the go-to tool for bridging across voids, building paths in BedWars-style games, or covering open ground quickly and consistently.

The **Technique** setting picks how you bridge: *Normal* handles everyday bridging, while *GodBridge* and *Breezily* are fast, sprint-friendly diagonal styles, and *Expand* reaches out to place a run of blocks ahead of you. Holding jump with a **Tower** mode selected lets you stack straight up. A large set of optional toggles — **Strafe**, **Acceleration**, **SpeedLimiter**, **SprintControl** and **StrafeOnJump** — tune how fast you move and how your movement looks to anti-cheats, while **Blink** can briefly hold back your packets to hide placements.

Scaffold also bundles convenience features so you don't need extra modules running: it can pull in [SafeWalk](/docs/modules/movement/safewalk) edge protection, an [Eagle](/docs/modules/player/eagle)-style auto-sneak so you don't slip off, and an **AutoSpeed** toggle that temporarily enables [Speed](/docs/modules/movement/speed) while you bridge. AutoBlock automatically grabs a suitable block from your inventory, and the built-in **Ledge** helper jumps or sneaks at edges to keep you from falling.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Delay | Integer Range | 0..0 | 0..40 ticks | Adds a wait between placements; raise it to slow down and look more human. |
| MinDist | Decimal | 0.0 | 0.0..0.25 | Requires the placement point to be at least this far from your eyes before a block is placed. |
| Timer | Decimal | 1.0 | 0.01..10.0 | Speeds up or slows down the game clock while bridging; above 1.0 places blocks faster. |
| BlockItemSelection | Setting Group | — | — | Controls which blocks Scaffold is allowed to use. |
| BlockItemSelection → Disallowed | Registry List | — | — | Blocks that will never be placed or counted as building material (e.g. TNT, cobwebs). |
| BlockItemSelection → Unfavorable | Registry List | — | — | Blocks used only as a last resort when nothing better is available (e.g. crafting tables). |
| AutoBlock | Toggleable Group | On | — | Automatically selects and holds a placeable block from your hotbar/inventory. |
| AutoBlock → Always | Toggle | true | — | Keeps a block held at all times rather than only switching at the moment of placing. |
| AutoBlock → SlotResetDelay | Integer | 0 | 0..40 ticks | How long to wait before switching your hotbar slot back after placing. |
| AutoBlock → DoNotUseBelowCount | Integer | 5 | 0..64 | Avoids using a stack once it drops to this size, saving your last few blocks. |
| Prediction | Toggleable Group | On | — | Aims ahead to where you'll actually stand when the block is placed, for smoother bridging. |
| Prediction → BootstrapBackoff | Decimal | 0.2 | 0.0..0.4 | How far behind the detected edge the early prediction sits before placement history builds up. |
| Prediction → PredictionCutoffDistance | Decimal | 0.05 | 0.0..0.3 | How close to the edge you can get before future-position prediction is switched off. |
| Prediction → WarmupPlacements | Integer | 2 | 0..4 | How many recorded placements it takes to blend fully into history-based prediction. |
| Technique | Mode Selector | Normal | — | Chooses the overall bridging style. |
| Technique → [Normal] → RotationMode | Choice | Stabilized | Center, Random, Stabilized, NearestRotation, ReverseYaw, DiagonalYaw, AngleYaw, EdgePoint | How your aim is positioned on the block face while placing. |
| Technique → [Normal] → RequiresSight | Toggle | true | — | Only places when the target block is actually in line of sight. |
| Technique → [Normal] → Eagle | Toggleable Group | Off | — | Auto-sneaks at edges so you don't fall off while placing. |
| Technique → [Normal] → Eagle → BlocksToEagle | Integer Range | 0..0 | 0..10 | How many blocks to place between each sneak cycle. |
| Technique → [Normal] → Eagle → EdgeDistance | Decimal Range | 0.01..0.05 | 0.01..1.3 | How close to the edge you must be before it sneaks. |
| Technique → [Normal] → Eagle → OnlyOnGround | Toggle | true | — | Only sneaks while standing on the ground. |
| Technique → [Normal] → Telly | Toggleable Group | Off | — | Jumps while moving for a faster, "telly bridge" style. |
| Technique → [Normal] → Telly → ResetMode | Choice | Reset | Reverse, Reset | How your aim resets between jumps. |
| Technique → [Normal] → Telly → Straight | Integer | 1 | 0..5 ticks | Air-time window used to decide whether you're bridging straight. |
| Technique → [Normal] → Telly → Jump | Integer Range | 0..0 | 0..10 ticks | Delay before each jump. |
| Technique → [Normal] → Telly → AimOnTower | Toggle | true | — | Keeps aiming at blocks while towering up. |
| Technique → [Normal] → Down | Toggleable Group | Off | — | Lets you bridge downward by sneaking. |
| Technique → [Normal] → StabilizeMovement | Toggleable Group | Off | — | Nudges your movement back toward the ideal line to keep placements centered. |
| Technique → [Normal] → Ceiling | Toggleable Group | Off | — | Builds a ceiling above you instead of a floor. |
| Technique → [Normal] → HeadHitter | Toggleable Group | Off | — | Auto-jumps into blocks above your head when bridging under a low ceiling. |
| Technique → [Expand] → Length | Integer | 5 | 1..10 blocks | How far ahead the expand technique reaches to place blocks. |
| Technique → [GodBridge] → Modes | Multi-Select | [Jump] | Jump, Sneak, StopInput, Backwards | Which actions are used to stay on the ledge while god-bridging. |
| Technique → [GodBridge] → ForceSneakBelowCount | Integer | 5 | 0..10 | Forces a sneak instead of other actions once your block count drops this low. |
| Technique → [GodBridge] → SneakTime | Integer Range | 1..1 | 1..10 | How long each forced sneak lasts. |
| Technique → [Breezily] → EdgeDistance | Decimal Range | 0.4..0.45 | 0.25..0.5 blocks | How far from the edge the breezily technique repositions you sideways. |
| SameY | Choice | Off | Off, On, Falling, Hypixel | Keeps placements on a single height level instead of stepping down. |
| Tower | Mode Selector | None | — | How Scaffold builds straight up when you hold jump. |
| Tower → [Motion] → Motion | Decimal | 0.42 | 0.0..1.0 | Upward boost applied each tower step. |
| Tower → [Motion] → TriggerHeight | Decimal | 0.78 | 0.76..1.0 | How high above the jump point you must rise before the next boost. |
| Tower → [Motion] → Slow | Decimal | 0.6 | 0.0..3.0 | Horizontal slowdown while towering to keep you centered. |
| Tower → [Pulldown] → Trigger | Decimal | 0.1 | 0.0..0.2 Y/v | Vertical speed at which you get pulled back down for the next placement. |
| Tower → [Karhu] → Timer | Decimal | 1.0 | 0.1..10.0 | Game-clock speed used during this tower mode. |
| Tower → [Karhu] → Trigger | Decimal | 0.06 | 0.0..0.2 Y/v | Vertical speed at which the pulldown kicks in. |
| Tower → [Karhu] → Pulldown | Toggle | true | — | Pulls you back down after each rise to place the next block. |
| SafeWalk | Mode Selector | None | None, Safe, OnEdge | Stops you walking off edges while bridging. |
| SafeWalk → [OnEdge] → Distance | Decimal Range | 0.1..0.15 | 0.05..0.5 | How close to the edge the protection activates. |
| SafeWalk → [OnEdge] → Keep | Integer Range | 1..2 | 1..20 ticks | How long the edge reaction is held. |
| SafeWalk → [OnEdge] → Mode | Choice | Stop | Stop, Invert, Center | How your movement is corrected at the edge. |
| SafeWalk → [OnEdge] → Sneak | Integer Range | 0..0 | 0..20 ticks | How long to sneak when reaching an edge. |
| SafeWalk → [OnEdge] → Jump | Toggle | false | — | Allows jumping as part of the edge reaction. |
| Swing | Choice | HideForClient | DoNotHide, HideForBoth, HideForClient, HideForServer | Controls whether your hand-swing animation is shown to you and/or the server. |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| SprintControl | Toggleable Group | Off | — | Forces sprinting on or off independently for the client and server. |
| SprintControl → Client | Choice | DoNotChange | DoNotChange, ForceSprint, ForceNoSprint, NoSprintOnPlace, NoSprintOnGround | How sprinting is handled on your own (visual) side. |
| SprintControl → Server | Choice | DoNotChange | DoNotChange, ForceSprint, ForceNoSprint, NoSprintOnPlace, NoSprintOnGround | How sprinting is reported to the server. |
| SimulatePlacementAttempts | Toggleable Group | Off | — | Sends extra interaction clicks to mimic a real player placing blocks. |
| SimulatePlacementAttempts → Clicker | Setting Group | — | — | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| SimulatePlacementAttempts → FailedAttemptsOnly | Toggle | false | — | Only simulates clicks that wouldn't actually place a block. |
| Acceleration | Toggleable Group | Off | — | Multiplies your horizontal speed while bridging. |
| Acceleration → SpeedMultiplier | Decimal | 1.11 | 0.1..3.0 | How much your movement speed is scaled. |
| Acceleration → OnlyOnGround | Toggle | true | — | Only applies the boost while on the ground. |
| Strafe | Toggleable Group | Off | — | Continuously adjusts your velocity to keep a steady bridging speed. |
| Strafe → Speed | Decimal | 0.19 | 0.0..5.0 | Target movement speed while strafing. |
| Strafe → Hypixel | Toggle | false | — | Uses speed values tuned to pass on Hypixel. |
| Strafe → OnlyOnGround | Toggle | true | — | Only strafes while on the ground. |
| StrafeOnJump | Toggleable Group | Off | — | Applies a speed burst each time you jump while bridging. |
| StrafeOnJump → StraightSpeed | Decimal Range | 0.48..0.49 | 0.1..1.0 | Speed applied when moving straight. |
| StrafeOnJump → DiagonalSpeed | Decimal Range | 0.48..0.49 | 0.1..1.0 | Speed applied when moving diagonally. |
| SpeedLimiter | Toggleable Group | Off | — | Caps your bridging speed by cutting movement when you go too fast. |
| SpeedLimiter → SpeedLimit | Decimal | 0.12 | 0.01..0.4 | The maximum horizontal speed allowed. |
| Blink | Toggleable Group | Off | — | Briefly holds back your outgoing packets around placements to hide them. |
| Blink → Time | Integer Range | 0..0 | 0..3000 ms | How long packets are held after each placement. |
| Blink → FlushOn | Multi-Select | [] | Place, Towering, Sneaking, NotSneaking, OnGround, InAir | Conditions that immediately release the held packets. |
| AutoSpeed | Toggle | false | — | Temporarily enables [Speed](/docs/modules/movement/speed) while Scaffold is active. |
| Ledge | Toggle | true | — | Auto-jumps or auto-sneaks at edges so you don't fall while placing. |
| Render | Toggleable Group | On | — | See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/scaffold/ModuleScaffold.kt)*
