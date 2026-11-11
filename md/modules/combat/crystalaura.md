## CrystalAura

CrystalAura places end crystals next to your enemy and blows them up right away. Crystals do a lot of damage, so this is the main module for crystal PvP. It only uses spots where the explosion hurts the enemy much more than you. You need end crystals, and obsidian or bedrock to place them on.

For crystal PvP it works well with [Surround](/docs/modules/world/surround) and [AutoTrap](/docs/modules/world/autotrap). CrystalAura turns off when you leave a server.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Target | Setting Group | | | See [Shared: Target](/docs/modules/shared-settings/target). Its Range (default 4.5, 1.0..12.0) sets how far away enemies can be. |
| Place | Toggleable Group | On | | Places crystals. Turn it off to only break crystals. |
| Place → Swing | Choice | DoNotHide | DoNotHide, HideForClient | Whether you see your arm swing when placing. |
| Place → Switch | Choice | Silent | Silent, Normal, None | How to switch to crystals. Silent switches without you seeing it. Normal switches your held item. None never switches. |
| Place → 1_12_2 | Toggle | false | | Uses the rules from Minecraft 1.12.2, where a crystal needs two empty blocks above it. |
| Place → Delay | Integer | 0 | 0..1000 ms | How long to wait between placing crystals. |
| Place → Range | Decimal | 4.5 | 1.0..6.0 | How far away you can place crystals, in blocks. |
| Place → WallsRange | Decimal | 4.5 | 0.0..6.0 | How far away you can place crystals behind blocks. |
| Place → OnlyAbove | Toggle | false | | Only clicks on the top side of blocks. |
| Place → Sequenced | Toggle | false | | Places in a way some servers expect. Try it if placing does not work. |
| Place → NotFacingAway | Toggle | false | | Does not click on block sides that face away from you. Only when OnlyAbove is off. |
| Place → Jitter | Toggle | false | | Moves your aim a tiny bit between placements. Only when OnlyAbove is off. |
| Place → TargetRendering | Toggleable Group | On | | See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |
| Destroy | Toggleable Group | On | | Hits crystals to blow them up. |
| Destroy → Swing | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Whether your arm swing is shown when hitting a crystal, to you, to the server, or to both. |
| Destroy → Delay | Integer | 0 | 0..1000 ms | How long to wait between hitting crystals. |
| Destroy → Range | Decimal | 4.5 | 1.0..6.0 | How far away you can hit crystals, in blocks. |
| Destroy → WallsRange | Decimal | 4.5 | 0.0..6.0 | How far away you can hit crystals behind blocks. |
| Destroy → PrioritizeVisibleFaces | Toggle | false | | Prefers to hit the side of the crystal you can see. Looks more like a real player but can be slower. |
| Damage | Setting Group | | | Decides if a crystal is worth placing or breaking. |
| Damage → MaxSelfDamage | Decimal | 2.0 | 0.0..10.0 | Skips crystals that would hurt you more than this. |
| Damage → MaxFriendDamage | Decimal | 1.0 | 0.0..10.0 | Skips crystals that would hurt a friend more than this. |
| Damage → MinEnemyDamage | Decimal | 5.0 | 0.0..10.0 | Only uses crystals that hurt the enemy at least this much. |
| Damage → AntiSuicide | Toggle | true | | Never uses a crystal that would kill you. |
| Damage → Efficient | Toggle | true | | Only uses crystals that hurt the enemy more than you. |
| Damage → Terrain | Toggle | true | | Counts blocks the explosion would break as gone, which gives better damage numbers. |
| Triggers | Setting Group | | | What makes CrystalAura check again for crystals to place or break. |
| Triggers → NotWhileUsingItem | Toggle | false | | Waits while you eat, drink or block. |
| Triggers → Off-Thread | Toggle | true | | Does the math in the background so your game does not lag. |
| Triggers → Tick | Toggle | true | | Checks every tick. |
| Triggers → BlockChange | Toggle | true | | Checks when a block nearby changes, for example when the enemy's protection gets broken. |
| Triggers → ClientBlockBreak | Toggle | true | | Checks when you break a block, even before the server says so. Useful with [PacketMine](/docs/modules/world/packetmine). |
| Triggers → CrystalSpawn | Toggle | true | | Checks when a crystal appears. |
| Triggers → CrystalDestroy | Toggle | true | | Checks when a crystal disappears. |
| Triggers → ExplodeSound | Toggle | true | | Checks when an explosion sound plays. |
| Triggers → EntityMove | Toggle | true | | Checks when a player or mob nearby moves. |
| Triggers → SelfMove | Toggle | false | | Checks when you move. |
| Predict | Setting Group | | | Guesses where you and the target will be soon. |
| Predict → Self | Toggleable Group | On | | Guesses where you will be soon and uses that for the damage checks. |
| Predict → Self → PlaceTicks | Integer | 2 | 0..20 | How many ticks (20 per second) ahead to guess when placing. |
| Predict → Self → BreakTicks | Integer | 1 | 0..20 | How many ticks ahead to guess when breaking. |
| Predict → Self → BasePlaceTicks | Integer | 4 | 0..20 | How many ticks ahead to guess when building a base. |
| Predict → Self → CalculationMode | Choice | Both | Both, PredictOnly | Both checks the damage now and the guessed damage. PredictOnly only checks the guessed damage. |
| Predict → Self → CalculationMode → [Both] → Logic | Choice | And | And, Or | And: both checks must pass. Or: one of them is enough. |
| Predict → Self → CheckIntersect | Toggle | true | | Skips spots where you will be standing. |
| Predict → Target | Toggleable Group | On | | Guesses where the target will be soon and uses that for the damage checks. |
| Predict → Target → PlaceTicks | Integer | 2 | 0..20 | How many ticks (20 per second) ahead to guess when placing. |
| Predict → Target → BreakTicks | Integer | 1 | 0..20 | How many ticks ahead to guess when breaking. |
| Predict → Target → BasePlaceTicks | Integer | 4 | 0..20 | How many ticks ahead to guess when building a base. |
| Predict → Target → CalculationMode | Choice | Both | Both, PredictOnly | Both checks the damage now and the guessed damage. PredictOnly only checks the guessed damage. |
| Predict → Target → CalculationMode → [Both] → Logic | Choice | And | And, Or | And: both checks must pass. Or: one of them is enough. |
| Predict → Target → CheckIntersect | Toggle | true | | Skips spots where the target will be standing. |
| IDPredict | Toggleable Group | Off | | Hits a new crystal right after placing it, before the server says it is there. Very fast, but can fail. |
| IDPredict → OffsetRange | Integer Range | 1..2 | 1..100 | How many guesses to try for the new crystal. |
| IDPredict → SwingAlways | Toggle | false | | Swings your arm for every guess, not only once. |
| IDPredict → Rotate | Toggleable Group | On | | Turns toward the crystal before hitting it. |
| IDPredict → Rotate → Back | Toggle | false | | Turns back afterwards. |
| SetDead | Toggleable Group | On | | Removes a crystal you hit right away, without waiting for the server, so the next one can be placed sooner. |
| SetDead → ConfirmTime | Integer | 150 | 10..2000 ms | If the server does not confirm the crystal is gone after this long, it comes back. |
| BasePlace | Toggleable Group | On | | Places obsidian or bedrock to make better spots for crystals. |
| BasePlace → CalcDelay | Integer | 120 | 0..1000 ms | How long to wait before looking for a new spot to build. |
| BasePlace → TimeOut | Integer | 240 | 0..5000 ms | Gives up on a planned block after this long. |
| BasePlace → PlatformOnly | Toggle | false | | Only builds right under the enemy. |
| BasePlace → OnlyAboveSelf | Toggle | false | | Only builds at your height or higher, so you don't give the enemy a place to stand. |
| BasePlace → Terrain | Toggle | true | | Like Damage → Terrain, but for building. Only works when Damage → Terrain is on. |
| BasePlace → SimulateMovement | Toggleable Group | On | | Makes sure you won't walk into the block it places. |
| BasePlace → SimulateMovement → Ticks | Integer | 3 | 1..20 | How many ticks of your walking to look ahead. |
| BasePlace → SimulateMovement → Error | Decimal | 0.1 | 0.0..2.0 | Extra space kept around you per tick. |
| BasePlace → SimulateMovement → ErrorStep | Decimal | 0.05 | 0.0..1.0 | How much that extra space grows each tick. |
| BasePlace → SimulateMovement → DownError | Toggle | false | | Also keeps the extra space below you. |
| BasePlace → SimulateMovement → AntiPlatformSimulate | Toggle | true | | Does not build where you might step up onto. |
| BasePlace → MinAdvantage | Decimal | 2.0 | 0.1..10.0 | How much more damage a built spot has to do than an existing spot to be worth building. |
| BasePlace → Placing | Setting Group | | | See [Shared: Block Placer](/docs/modules/shared-settings/block-placer). |
| TargetRendering | Toggleable Group | On | | See [Shared: TargetRendering](/docs/modules/shared-settings/targetrendering). |
| RotationMode | Choice | Normal | Normal, None | Whether you turn toward the crystal. Normal turns you. None does not. |
| RotationMode → [Normal] → PostMove | Toggle | false | | Turns after you move instead of before. |
| RotationMode → [Normal] → Instant | Toggle | false | | Turns right away. |
| RotationMode → [Normal] → Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| RotationMode → [Normal] → IgnoreOpenInventory | Toggle | true | | Keeps turning while your inventory is open. |
| RotationMode → [None] → PostMove | Toggle | false | | Sends the action after you move instead of before. |
| RotationMode → [None] → Instant | Toggle | false | | Acts right away. |
| RotationMode → [None] → SendRotationPacket | Toggle | false | | Still tells the server where you look. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/crystalaura/ModuleCrystalAura.kt)*
