## CrystalAura

CrystalAura is the all-in-one tool for crystal PvP: it automatically places end crystals next to your target and then attacks them to detonate, dealing huge burst damage. When enabled it constantly scans for the best spot where an explosion hurts the enemy far more than it hurts you, places a crystal there (using obsidian or bedrock as a base), and breaks it the instant it appears. Built-in damage checks keep you from blowing yourself up, and it only ever acts on positions that clear your thresholds. It's also known by its alias *AutoCrystal*.

It pairs naturally with crystal-PvP setups — for example [Surround](/docs/modules/world/surround) and [AutoTrap](/docs/modules/world/autotrap) to protect yourself, and it can react to client-side block breaks from [PacketMine](/docs/modules/world/packetmine). The many triggers, prediction options, and the BasePlace builder let you tune it for anything from a legit tick-based aura to an extremely fast, ID-predicting double. CrystalAura turns itself off when you leave a server.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |
| Place | Toggleable Group | On | — | Whether (and how) CrystalAura places crystals. Turn off to only destroy. |
| Place → Swing | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Whether and to whom your arm swing is shown when placing. |
| Place → Switch | Choice | Silent | Silent, Normal, None | How the client switches to your crystals — silently, like a normal hotbar swap, or not at all. |
| Place → 1_12_2 | Toggle | false | — | Use 1.12.2-style placement rules (requires two air blocks above the base). |
| Place → Delay | Integer | 0 | 0..1000 ms | Minimum wait between placements. |
| Place → Range | Decimal | 4.5 | 1.0..6.0 | Maximum reach for placing crystals you can see. |
| Place → WallsRange | Decimal | 4.5 | 0.0..6.0 | Maximum reach for placing through walls/blocks. |
| Place → OnlyAbove | Toggle | false | — | Only place on the top face of blocks. Outdated and usually not recommended. |
| Place → Sequenced | Toggle | false | — | Place using a sequenced (confirmed) interaction, which can be safer on some servers. |
| Place → NotFacingAway | Toggle | false | — | Avoid placing on block faces that point away from you. Only applies without OnlyAbove. |
| Place → Jitter | Toggle | false | — | Slightly varies aim between placements. Only applies without OnlyAbove. |
| Place → TargetRendering | Toggleable Group | On | — | See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |
| Destroy | Toggleable Group | On | — | Whether (and how) CrystalAura attacks crystals to detonate them. |
| Destroy → Swing | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Whether and to whom your arm swing is shown when breaking. |
| Destroy → Delay | Integer | 0 | 0..1000 ms | Minimum wait between attacks. |
| Destroy → Range | Decimal | 4.5 | 1.0..6.0 | Maximum reach for breaking crystals you can see. |
| Destroy → WallsRange | Decimal | 4.5 | 0.0..6.0 | Maximum reach for breaking through walls/blocks. |
| Destroy → PrioritizeVisibleFaces | Toggle | false | — | Prefer crystal faces you can actually see. More legit, but may slow the aura down. |
| Damage | Setting Group | — | — | Thresholds that decide whether a crystal is worth placing or breaking. |
| Damage → MaxSelfDamage | Decimal | 2.0 | 0.0..10.0 | Won't act if the explosion would deal you more than this much damage. |
| Damage → MaxFriendDamage | Decimal | 1.0 | 0.0..10.0 | Won't act if it would deal a friend more than this much damage. |
| Damage → MinEnemyDamage | Decimal | 3.0 | 0.0..10.0 | Only acts if the enemy would take at least this much damage. |
| Damage → AntiSuicide | Toggle | true | — | Never place or break a crystal that would kill you. |
| Damage → Efficient | Toggle | true | — | Only act when the enemy takes more damage than you do. |
| Damage → Terrain | Toggle | true | — | Ignores blocks the blast would destroy when estimating damage, for more accurate numbers. |
| Triggers | Setting Group | — | — | Which game events cause CrystalAura to recheck and act. |
| Triggers → NotWhileUsingItem | Toggle | false | — | Pause while you're using an item (eating, drinking, blocking) to avoid anticheat flags. |
| Triggers → Off-Thread | Toggle | true | — | Run calculations on a separate thread to reduce FPS impact. |
| Triggers → Tick | Toggle | true | — | Act every tick. The most legit trigger. |
| Triggers → BlockChange | Toggle | true | — | React the moment a block is broken in the aura's area, e.g. to instantly fill enemy surrounds. |
| Triggers → ClientBlockBreak | Toggle | true | — | React even earlier on blocks broken client-side (useful with [PacketMine](/docs/modules/world/packetmine)). |
| Triggers → CrystalSpawn | Toggle | true | — | React when a crystal spawns. |
| Triggers → CrystalDestroy | Toggle | true | — | React when a crystal is removed. |
| Triggers → ExplodeSound | Toggle | true | — | React when an explosion sound is received. |
| Triggers → EntityMove | Toggle | true | — | React when a nearby entity moves. |
| Triggers → SelfMove | Toggle | false | — | React when you move. |
| Predict | Setting Group | — | — | Uses simulated future positions to judge damage and placement. |
| Predict → Self | Toggleable Group | On | — | Predict your own future position. |
| Predict → Self → PlaceTicks | Integer | 2 | 0..20 | Ticks ahead to predict for placing (roughly 20 ÷ your crystals-per-second). |
| Predict → Self → BreakTicks | Integer | 1 | 0..20 | Ticks ahead to predict for breaking. Normally lower than PlaceTicks. |
| Predict → Self → BasePlaceTicks | Integer | 4 | 0..20 | Ticks ahead to predict for base-place. Normally higher than PlaceTicks. |
| Predict → Self → CalculationMode | Mode Selector | Both | Both, PredictOnly | How the predicted data is used for damage calculation. |
| Predict → Self → CalculationMode → [Both] → Logic | Choice | And | And, Or | Combine the current and predicted damage values with And or Or. |
| Predict → Self → CheckIntersect | Toggle | true | — | Skip spots your predicted position would block. |
| Predict → Target | Toggleable Group | On | — | Predict the target's future position. |
| Predict → Target → PlaceTicks | Integer | 2 | 0..20 | Ticks ahead to predict for placing (roughly 20 ÷ your crystals-per-second). |
| Predict → Target → BreakTicks | Integer | 1 | 0..20 | Ticks ahead to predict for breaking. Normally lower than PlaceTicks. |
| Predict → Target → BasePlaceTicks | Integer | 4 | 0..20 | Ticks ahead to predict for base-place. Normally higher than PlaceTicks. |
| Predict → Target → CalculationMode | Mode Selector | Both | Both, PredictOnly | How the predicted data is used for damage calculation. |
| Predict → Target → CalculationMode → [Both] → Logic | Choice | And | And, Or | Combine the current and predicted damage values with And or Or. |
| Predict → Target → CheckIntersect | Toggle | true | — | Skip spots the target's predicted position would block. |
| IDPredict | Toggleable Group | On | — | Sends the break packet instantly by guessing the new crystal's entity ID, for very fast doubles. |
| IDPredict → OffsetRange | Integer Range | 1..2 | 1..100 | Range of entity-ID offsets to attack. |
| IDPredict → SwingAlways | Toggle | false | — | Swing before every attack instead of only once. |
| IDPredict → Rotate | Toggleable Group | On | — | Send an extra rotation packet before the predicted attack. |
| IDPredict → Rotate → Back | Toggle | false | — | Rotate back to your original view afterward. |
| SetDead | Toggleable Group | On | — | Instantly removes hit crystals from the world instead of waiting for the server, allowing faster re-placement. |
| SetDead → ConfirmTime | Integer | 150 | 10..2000 ms | How long to wait before restoring a crystal if no confirmation arrives. |
| BasePlace | Toggleable Group | On | — | Builds obsidian/bedrock bases to create better crystal spots. |
| BasePlace → CalcDelay | Integer | 120 | 0..1000 ms | How long to wait before starting a new base-place calculation. |
| BasePlace → TimeOut | Integer | 240 | 0..5000 ms | After this long, the planned base placement is cleared. |
| BasePlace → PlatformOnly | Toggle | false | — | Only build directly below the enemy. |
| BasePlace → OnlyAboveSelf | Toggle | false | — | Only build at or above your own level, so you don't help the enemy. |
| BasePlace → Terrain | Toggle | true | — | Exclude terrain for base-place damage estimates. Only has an effect when Damage → Terrain is on. |
| BasePlace → SimulateMovement | Toggleable Group | On | — | Make sure you won't walk into the base placement. |
| BasePlace → SimulateMovement → Ticks | Integer | 3 | 1..20 | How many ticks of your movement are simulated. |
| BasePlace → SimulateMovement → Error | Decimal | 0.1 | 0.0..2.0 | How much your hitbox grows per simulated tick. |
| BasePlace → SimulateMovement → ErrorStep | Decimal | 0.05 | 0.0..1.0 | How much the growth increases each tick. |
| BasePlace → SimulateMovement → DownError | Toggle | false | — | Also extend the simulated hitbox downward. |
| BasePlace → SimulateMovement → AntiPlatformSimulate | Toggle | true | — | Exclude levels you might step onto, so you don't build a platform for the enemy. |
| BasePlace → MinAdvantage | Decimal | 2.0 | 0.1..10.0 | Extra damage a base-place spot must offer over a normal spot to be worth it. |
| BasePlace → Placing | Setting Group | — | — | See [Shared: Block Placer](/docs/modules/shared-settings/block-placer). |
| TargetRendering | Toggleable Group | On | — | See [Shared: TargetRendering](/docs/modules/shared-settings/target-rendering). |
| RotationMode | Mode Selector | Normal | Normal, None | How the client aims when placing and breaking. |
| RotationMode → [Normal] → PostMove | Toggle | false | — | Apply the rotation after movement. |
| RotationMode → [Normal] → Instant | Toggle | false | — | Snap to the rotation instantly. |
| RotationMode → [Normal] → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| RotationMode → [Normal] → IgnoreOpenInventory | Toggle | true | — | Keep rotating even while your inventory is open. |
| RotationMode → [None] → PostMove | Toggle | false | — | Apply the rotation after movement. |
| RotationMode → [None] → Instant | Toggle | false | — | Snap to the rotation instantly. |
| RotationMode → [None] → SendRotationPacket | Toggle | false | — | Send a rotation packet even though no aiming is performed. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/crystalaura/ModuleCrystalAura.kt)*
