## KillAura

KillAura attacks enemies near you by itself. It picks a target in range, turns you toward it and hits it as fast as your [Clicker](/docs/modules/shared-settings/clicker) settings allow. You don't need to aim or click.

<video src="/images/modules/killaura/fightbot.mp4" controls width="600">Your browser does not support the video tag.</video>

[Velocity](/docs/modules/combat/velocity) and [AutoWeapon](/docs/modules/combat/autoweapon) go well with KillAura.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Clicker | Setting Group | | | How fast KillAura clicks. See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Clicker → ItemCooldown → IgnoreOnShieldBreak | Toggle | true | | Does not wait for the attack to charge when [AutoWeapon](/docs/modules/combat/autoweapon) will break the enemy's shield with an axe. |
| Clicker → ItemCooldown → IgnoreOnMaceSmash | Toggle | true | | Does not wait for the attack to charge when you can do a Mace smash attack. |
| Clicker → ItemCooldown → IgnoreWhenExitingRange | Toggle | true | | Does not wait for the attack to charge when the enemy is about to get out of reach. |
| Range | Setting Group | | | How far KillAura reaches. See [Shared: Range](/docs/modules/shared-settings/range). Here RangeIncrease starts at 1.0 and ThroughWallsRange at 3.0. |
| Range → ScanRangeIncrease | Decimal Range | 2.0..3.0 | 0.0..7.0 blocks | How much further than your reach KillAura already looks for enemies and turns toward them. |
| Target | Setting Group | | | See [Shared: Target](/docs/modules/shared-settings/target). |
| Target → IgnoreShield | Toggle | true | | Also attacks enemies that block with a shield. |
| Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Rotations → RotationTiming | Choice | Normal | Normal, Snap, OnTick | When you turn toward the enemy. Normal turns all the time. Snap only turns right when you hit. OnTick turns in the same tick as the hit. |
| Rotations → ThroughWalls | Toggle | false | | Also turns toward enemies behind blocks. |
| Rotations → LazyRotation | Toggle | false | | Does not turn if you are already looking at the enemy. |
| AimPoint | Setting Group | | | See [Shared: AimPoint](/docs/modules/shared-settings/aimpoint). |
| Requires | Multi-Select | | Click, Weapon, EmptyHand, VanillaName, NotBreaking | Only attacks when all picked conditions are true. Click: you are holding attack. Weapon: you hold a weapon. EmptyHand: your hand is empty. VanillaName: your item has no custom name. NotBreaking: you are not mining a block. |
| Raycast | Choice | All | None, Enemy, All | What happens when something stands between you and your target. All hits whatever is in the way. Enemy only hits it if it is an enemy too. None always hits your target. |
| Criticals | Choice | Smart | Smart, Ignore, Always | When to wait for a critical hit. Smart waits when a critical hit is possible soon. Ignore never waits. Always only hits when it is a critical hit. |
| KeepSprint | Toggle | true | | Keeps you sprinting when you hit. |
| IgnoreOpenInventory | Toggle | true | | Keeps attacking while your inventory or a chest is open. |
| SimulateInventoryClosing | Toggle | true | | Tells the server your inventory is closed before each hit. |
| AutoBlocking | Toggleable Group | Off | | Blocks with your shield or sword between hits. |
| AutoBlocking → BlockMode | Choice | Interact | Basic, Interact, Fake | How you block. Basic just uses the item. Interact also clicks the entity or block you look at. Fake only shows the blocking animation and does not really block. |
| AutoBlocking → SimulateVanillaUse | Toggle | true | | Blocks the same way a normal right click would. |
| AutoBlocking → UnblockMode | Choice | StopUsingItem | StopUsingItem, ChangeSlot, SwapHand, None | How you stop blocking before a hit. StopUsingItem lets go of the item. ChangeSlot switches your held item for a moment. SwapHand swaps your hands twice. None keeps blocking. |
| AutoBlocking → Reblock | Integer Range | 0..0 | 0..3 ticks | How long to wait after a hit before blocking again, in ticks (20 per second). |
| AutoBlocking → PauseOnUnblock | Integer Range | 0..0 | 0..3 ticks | How long to wait after you stop blocking before hitting. |
| AutoBlocking → Chance | Decimal | 100.0 | 0.0..100.0 % | How often it blocks. |
| AutoBlocking → Blink | Integer | 0 | 0..10 ticks | How long to hold back your movement while blocking, so you look laggy. |
| AutoBlocking → PrioritizeBlocking | Toggle | true | | Waits until you are really blocking before it hits, so you hit a bit slower. |
| AutoBlocking → OnScanRange | Toggle | true | | Already blocks when an enemy is close but not yet in reach. |
| AutoBlocking → OnlyWhenInDanger | Toggleable Group | Off | | Only blocks when an enemy is looking at you and can reach you. |
| AutoBlocking → OnlyWhenInDanger → Tolerance | Decimal | 0.3 | 0.0..1.0 blocks | How close the enemy's aim has to be to you to count. Higher blocks more often. |
| AutoBlocking → OnlyWhenInDanger → ForceActiveRange | Decimal Range | 0.0..1.0 | 0.0..6.0 | Always blocks when the enemy is this close, no matter where they look. |
| AutoBlocking → AssumeShield | Toggle | false | | Turn this on when you play on a 1.8 server from a newer version, where the server gives you a shield when you block. |
| TargetRendering | Toggleable Group | On | | See [Shared: TargetRendering](/docs/modules/shared-settings/targetrendering). |
| FailSwing | Toggleable Group | Off | | Swings your arm at enemies that are a bit too far away, like a real player who misses. |
| FailSwing → AdditionalRange | Decimal Range | 2.5..3.0 | 0.0..10.0 | How much further than your reach it still swings. |
| FailSwing → NotifyWhenFail | Choice | Box | None, Box, Sound | What happens when you miss. Box draws a small box where you missed. Sound plays a sound. None does nothing. |
| FailSwing → NotifyWhenFail → [Box] → Fade | Integer | 4 | 1..10 secs | How long the box stays. |
| FailSwing → NotifyWhenFail → [Box] → Color | Color | | | Color of the box. |
| FailSwing → NotifyWhenFail → [Box] → Rainbow | Toggle | false | | Makes the box rainbow colored. |
| FailSwing → NotifyWhenFail → [Sound] → Volume | Decimal | 50.0 | 0.0..100.0 | How loud the sound is. |
| FailSwing → NotifyWhenFail → [Sound] → Pitch | Decimal | 0.8 | 0.0..2.0 | How high the sound is. |
| FightBot | Toggleable Group | Off | | Walks you to enemies and fights them for you. See [Shared: AutoWalk](/docs/modules/shared-settings/autowalk) for the walking settings. |
| FightBot → OpponentRange | Decimal | 3.0 | 0.1..10.0 | How far the enemy can reach you, in blocks. |
| FightBot → DangerousYaw | Decimal | 55.0 | 0.0..90.0 ° | When the enemy looks at you closer than this angle, you are in danger. |
| FightBot → RunawayOnCooldown | Toggle | true | | Walks away from the enemy while your attack is charging. |
| FightBot → TargetFilter → Range | Decimal | 50.0 | 10.0..100.0 | How far away enemies can be to walk to them, in blocks. |
| FightBot → TargetFilter → VisibleOnly | Toggle | true | | Only walks to enemies you can see. |
| FightBot → TargetFilter → NotWhenVoid | Toggle | true | | Does not walk to enemies over the void. |
| FightBot → Leader | Toggleable Group | Off | | Follows a player when there is no enemy. |
| FightBot → Leader → Username | Text | | | The name of the player to follow. |
| FightBot → Leader → Radius | Decimal | 5.0 | 2.0..10.0 | How close to stay to that player, in blocks. |
| RangeIndicator | Toggleable Group | Off | | Draws a circle on the ground that shows how far KillAura reaches. |
| RangeIndicator → ColorMode | Choice | Static | Static, Rainbow, Distance | How the circle is colored. Static uses IdleColor and ActiveColor. Rainbow goes through all colors. Distance changes color by how close the target is. |
| RangeIndicator → IdleColor | Color | | | Color when there is no target. |
| RangeIndicator → ActiveColor | Color | | | Color when there is a target. |
| RangeIndicator → Outline | Toggle | true | | Draws a line around the edge of the circle. |
| RangeIndicator → OutlineColor | Color | | | Color of the edge line. |
| RangeIndicator → PulseAnimation | Toggle | false | | Makes the circle grow and shrink a little. |
| RangeIndicator → PulseSpeed | Decimal | 2.0 | 0.5..5.0 | How fast it grows and shrinks. |
| RangeIndicator → PulseIntensity | Decimal | 0.15 | 0.05..0.5 | How much it grows and shrinks. |
| RangeIndicator → FadeAnimation | Toggle | true | | Fades smoothly between IdleColor and ActiveColor. |
| RangeIndicator → FadeSpeed | Decimal | 0.1 | 0.01..0.5 | How fast it fades. |
| RangeIndicator → WallRangeColor | Color | | | Color of a second circle for the reach through walls. It is hidden by default. |
| RangeIndicator → ScanRangeColor | Color | | | Color of a circle for the scan range. It is hidden by default. |
| RangeIndicator → OpponentRangeColor | Color | | | Color of a circle for the enemy's reach. It is hidden by default. |
| RangeIndicator → HideWhenDead | Toggle | true | | Hides the circle while you are dead. |
| RangeIndicator → HideWhenSpectator | Toggle | true | | Hides the circle in spectator mode. |
| RangeIndicator → HideInVehicle | Toggle | false | | Hides the circle while you ride something. |
| RangeIndicator → RespectInventorySetting | Toggle | true | | Hides the circle when a chest is open and IgnoreOpenInventory is off. |
| RangeIndicator → CanBeCovered | Toggle | false | | Lets blocks hide the circle. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/killaura/ModuleKillAura.kt)*
