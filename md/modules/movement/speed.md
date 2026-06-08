## Speed

Speed lets you move significantly faster than Minecraft's normal sprint velocity by applying one of many bypass techniques, each tailored to a specific anti-cheat system. Choose the **Mode** that matches the server you are playing on — for example, `HypixelBHop` or `HypixelLowHop` for Hypixel's Watchdog, `Vulcan286` or `Vulcan288` for Vulcan, `NCP` for NoCheatPlus, `GrimCollide` for GrimAC, `BlocksMC` for BlocksMC, `Matrix7` for Matrix 7+, and so on. `LegitHop` is a subtle bunny-hop that works on many lenient servers, while `Custom` exposes every underlying parameter so you can craft your own bypass from scratch without writing any code.

The module has two optional conditional layers that each carry an independent copy of all bypass modes with separate, context-aware defaults. **OnlyInCombat** overrides the regular mode with a dedicated combat mode that only activates while you are engaged in combat, letting you move normally the rest of the time. **OnlyOnPotionEffect** activates a second separate mode exclusively when you have a Speed or Slowness potion effect within a configured amplifier range — useful on servers where potion-enhanced movement is expected and therefore less suspicious. Both layers are off by default and operate completely independently of each other and of the main mode.

The **Not** multi-select suppresses Speed whenever selected conditions are true (e.g., while using an item, sneaking, elytra-gliding, swimming, or while [Scaffold](/docs/modules/world/scaffold) is running). **AvoidEdgeBump** prevents the module from jumping when doing so would cause the player to bump into a block corner instead of stepping up cleanly. The **YawOffset** group subtly offsets the effective facing yaw to exploit the movement-direction bonus from strafing, gaining a small extra speed increment.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | LegitHop | — | Speed bypass technique to use. Available modes: LegitHop, Custom, YPort, PiercingAttack, VerusB3882, HypixelBHop, HypixelLowHop, Spartan-4.0.4.3, Spartan-4.0.4.3-FastFall, SentinelDamage, Vulcan286, Vulcan288, VulcanGround286, GrimCollide, NCP, Intave14, Intave14Fast, HylexLowHop, HylexGround, BlocksMC, Matrix7. Modes not listed below have no additional options. |
| Mode → [Custom] → HorizontalModification | Toggleable Group | off | — | Applies a constant horizontal speed factor each tick and/or a boost multiplier on jump. |
| Mode → [Custom] → HorizontalModification → HorizontalAcceleration | Decimal | 0.0 | -0.1..0.2 | Multiplies horizontal velocity by (1 + this value) every tick while moving. |
| Mode → [Custom] → HorizontalModification → HorizontalJumpOff | Decimal | 0.0 | -0.5..1.0 | Multiplies horizontal velocity by (1 + this value) when jumping off the ground. |
| Mode → [Custom] → HorizontalModification → TicksToBoostOff | Integer | 0 | 0..20 ticks | Delay in ticks before the HorizontalJumpOff boost is applied after leaving the ground. |
| Mode → [Custom] → VerticalModification | Toggleable Group | on | — | Adjusts jump height and vertical downward forces. |
| Mode → [Custom] → VerticalModification → JumpHeight | Decimal | 0.42 | 0.0..3.0 | Vertical velocity applied when jumping (vanilla default is 0.42). |
| Mode → [Custom] → VerticalModification → Pulldown | Decimal | 0.0 | 0.0..1.0 | Downward force subtracted each tick while the player is moving upward. |
| Mode → [Custom] → VerticalModification → PullDownDuringFall | Decimal | 0.25 | 0.0..1.0 | Downward force subtracted each tick while the player is falling. |
| Mode → [Custom] → TimerSpeed | Decimal | 1.0 | 0.1..10.0 | Game timer multiplier while moving; values above 1.0 speed up tick rate globally. |
| Mode → [Custom] → Strafe | Toggleable Group | on | — | Keeps movement direction optimised for speed when strafing. |
| Mode → [Custom] → Strafe → Strength | Decimal | 0.1 | 0.1..1.0 | How strongly strafe correction is blended in (1.0 = full correction). |
| Mode → [Custom] → Strafe → CustomSpeed | Toggle | false | — | When on, forces horizontal speed to the Speed value instead of using current momentum. |
| Mode → [Custom] → Strafe → Speed | Decimal | 0.25 | 0.1..10.0 | Target horizontal speed (blocks/tick) when CustomSpeed is enabled. |
| Mode → [Custom] → Strafe → VelocityTimeout | Integer | 20 | 0..20 ticks | Ticks to pause strafing after receiving a server velocity (knockback) packet. |
| Mode → [Custom] → Strafe → StrafeKnock | Toggle | true | — | Re-applies strafe direction after a server velocity packet to maintain momentum. |
| Mode → [YPort] → Speed | Decimal | 0.4 | 0.1..1.0 | Horizontal strafe speed applied immediately after each jump. |
| Mode → [PiercingAttack] → SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Controls whether the weapon swing animation is hidden when performing the piercing attack speed boost. |
| Mode → [PiercingAttack] → HoldTime | Integer Range | 1..1 | 1..20 ticks | Randomised tick range to silently hold the piercing weapon before restoring the hotbar slot. |
| Mode → [PiercingAttack] → OnGround | Toggle | true | — | Only perform the piercing attack boost while standing on the ground. |
| Mode → [PiercingAttack] → IgnoreHunger | Toggle | false | — | Use the boost even when hunger is too low to sprint normally. |
| Mode → [PiercingAttack] → WaitForCooldown | Toggle | true | — | Wait for the weapon's full attack cooldown before striking again. |
| Mode → [PiercingAttack] → MinimumDurability | Integer | 1 | 0..20 | Minimum remaining durability required on the piercing weapon before it is selected. |
| Mode → [HypixelBHop] → HorizontalAcceleration | Toggle | true | — | Adds a small horizontal speed boost each air tick, scaling with the Speed potion level. |
| Mode → [HypixelBHop] → VerticalAcceleration | Toggle | true | — | Reduces vertical descent slightly during early fall to maintain horizontal momentum. |
| Mode → [HypixelLowHop] → Glide | Toggle | true | — | Zeroes vertical velocity at air tick 7 when near the ground to prevent over-gliding. |
| Mode → [SentinelDamage] → Speed | Decimal | 0.5 | 0.1..5.0 | Horizontal strafe speed applied during the damage-boost phase. |
| Mode → [SentinelDamage] → ReboostTicks | Integer | 30 | 10..50 | Ticks between repeated boost packet cycles. |
| Mode → [GrimCollide] → BoostSpeed | Decimal | 0.08 | 0.01..0.08 b/t | Speed boost gained per nearby living entity during a collision check. |
| Mode → [GrimCollide] → ShrinkBox | Decimal | 0.5 | 0.1..2.0 | Expansion radius (blocks) of the detection box used to find nearby entities. |
| Mode → [NCP] → PullDown | Toggleable Group | off | — | Pulls the player downward at a specific air tick to shorten the jump arc. |
| Mode → [NCP] → PullDown → MotionMultiplier | Decimal | 1.0 | 0.01..10.0 | Scales the magnitude of the downward pull impulse. |
| Mode → [NCP] → PullDown → OnTick | Integer | 6 | 1..9 | Air tick at which the pull-down impulse fires. |
| Mode → [NCP] → PullDown → OnHurt | Toggle | false | — | Also applies a smaller downward impulse while the player is hurt and moving upward. |
| Mode → [NCP] → Boost | Toggleable Group | on | — | Applies a small constant horizontal speed multiplier each tick while moving. |
| Mode → [NCP] → Boost → InitialBoostMultiplier | Decimal | 1.0 | 0.01..10.0 | Scales the base per-tick horizontal boost constant. |
| Mode → [NCP] → Timer | Toggle | false | — | Requests a 1.08× game timer speed for additional throughput. |
| Mode → [NCP] → DamageBoost | Toggle | true | — | Boosts horizontal speed to at least 0.5 b/t while the player is hurt. |
| Mode → [NCP] → LowHop | Toggle | false | — | Reduces jump height to 0.4 to stay within NCP's speed tolerance. |
| Mode → [NCP] → AirStrafe | Toggle | true | — | Applies strafe correction while airborne. |
| Mode → [Intave14] → Strafe | Toggleable Group | on | — | Applies strafe optimisation while sprinting on the ground or at air tick 11. |
| Mode → [Intave14] → Strafe → Strength | Decimal | 0.29 | 0.01..0.27 | Strafe correction strength. |
| Mode → [Intave14] → AirBoost | Toggleable Group | on | — | Multiplies horizontal speed slightly while the player is ascending. |
| Mode → [Intave14Fast] → Timer | Toggle | true | — | Applies a 1.002× timer speed boost for a small additional movement gain. |
| Mode → [BlocksMC] → RoundStrafeYaw | Toggle | true | — | Rounds the movement yaw to the nearest 45° step when strafing. |
| Not | Multi-Select | [] | — | Suspends Speed while any selected condition is active: WhileUsingItem, DuringScaffold (also covers [Fly](/docs/modules/movement/fly)), WhileSneaking, IsFallFlying, IsInLiquid. |
| AvoidEdgeBump | Toggle | true | — | Delays jumps when the player would collide with a block corner rather than step up cleanly onto it. |
| OnlyInCombat | Toggleable Group | off | — | When enabled, the regular Mode is ignored and a separate combat-only mode activates exclusively while you are in combat. |
| OnlyInCombat → Mode | Mode Selector | HylexLowHop | — | Speed bypass mode used exclusively during combat. Same options as the top-level Mode. |
| OnlyInCombat → Mode → [Custom] → HorizontalModification | Toggleable Group | on | — | (Combat) Horizontal acceleration and jump-off boost. |
| OnlyInCombat → Mode → [Custom] → HorizontalModification → HorizontalAcceleration | Decimal | 0.0 | -0.1..0.2 | Multiplies horizontal velocity by (1 + this value) every tick while moving. |
| OnlyInCombat → Mode → [Custom] → HorizontalModification → HorizontalJumpOff | Decimal | 0.0 | -0.5..1.0 | Multiplies horizontal velocity by (1 + this value) when jumping off the ground. |
| OnlyInCombat → Mode → [Custom] → HorizontalModification → TicksToBoostOff | Integer | 0 | 0..20 ticks | Delay in ticks before the jump-off boost fires. |
| OnlyInCombat → Mode → [Custom] → VerticalModification | Toggleable Group | on | — | (Combat) Jump height and vertical pull-down forces. |
| OnlyInCombat → Mode → [Custom] → VerticalModification → JumpHeight | Decimal | 0.42 | 0.0..3.0 | Vertical velocity when jumping. |
| OnlyInCombat → Mode → [Custom] → VerticalModification → Pulldown | Decimal | 0.0 | 0.0..1.0 | Downward force while moving upward. |
| OnlyInCombat → Mode → [Custom] → VerticalModification → PullDownDuringFall | Decimal | 0.0 | 0.0..1.0 | Downward force while falling. |
| OnlyInCombat → Mode → [Custom] → TimerSpeed | Decimal | 1.0 | 0.1..10.0 | Timer multiplier while moving. |
| OnlyInCombat → Mode → [Custom] → Strafe | Toggleable Group | on | — | (Combat) Strafe correction. |
| OnlyInCombat → Mode → [Custom] → Strafe → Strength | Decimal | 1.0 | 0.1..1.0 | Strafe correction strength. |
| OnlyInCombat → Mode → [Custom] → Strafe → CustomSpeed | Toggle | false | — | Force horizontal speed to the Speed value. |
| OnlyInCombat → Mode → [Custom] → Strafe → Speed | Decimal | 1.0 | 0.1..10.0 | Target speed (blocks/tick) when CustomSpeed is on. |
| OnlyInCombat → Mode → [Custom] → Strafe → VelocityTimeout | Integer | 0 | 0..20 ticks | Ticks to pause strafing after a knockback packet. |
| OnlyInCombat → Mode → [Custom] → Strafe → StrafeKnock | Toggle | false | — | Re-applies strafe direction after a knockback packet. |
| OnlyInCombat → Mode → [YPort] → Speed | Decimal | 0.4 | 0.1..1.0 | Horizontal speed applied after each jump. |
| OnlyInCombat → Mode → [PiercingAttack] → SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Swing animation visibility during piercing attacks. |
| OnlyInCombat → Mode → [PiercingAttack] → HoldTime | Integer Range | 1..1 | 1..20 ticks | Ticks to silently hold the piercing weapon. |
| OnlyInCombat → Mode → [PiercingAttack] → OnGround | Toggle | true | — | Only boost while on the ground. |
| OnlyInCombat → Mode → [PiercingAttack] → IgnoreHunger | Toggle | false | — | Boost even when hunger is low. |
| OnlyInCombat → Mode → [PiercingAttack] → WaitForCooldown | Toggle | true | — | Wait for the attack cooldown before re-attacking. |
| OnlyInCombat → Mode → [PiercingAttack] → MinimumDurability | Integer | 1 | 0..20 | Minimum weapon durability required. |
| OnlyInCombat → Mode → [HypixelBHop] → HorizontalAcceleration | Toggle | true | — | Horizontal speed boost per air tick. |
| OnlyInCombat → Mode → [HypixelBHop] → VerticalAcceleration | Toggle | true | — | Reduces vertical descent during early fall. |
| OnlyInCombat → Mode → [HypixelLowHop] → Glide | Toggle | true | — | Zeroes vertical velocity at air tick 7 when near the ground. |
| OnlyInCombat → Mode → [SentinelDamage] → Speed | Decimal | 0.5 | 0.1..5.0 | Strafe speed during the damage-boost phase. |
| OnlyInCombat → Mode → [SentinelDamage] → ReboostTicks | Integer | 30 | 10..50 | Ticks between boost packet cycles. |
| OnlyInCombat → Mode → [GrimCollide] → BoostSpeed | Decimal | 0.08 | 0.01..0.08 b/t | Speed boost per nearby entity. |
| OnlyInCombat → Mode → [GrimCollide] → ShrinkBox | Decimal | 0.5 | 0.1..2.0 | Entity detection radius in blocks. |
| OnlyInCombat → Mode → [NCP] → PullDown | Toggleable Group | on | — | Pull-down impulse at a specific air tick. |
| OnlyInCombat → Mode → [NCP] → PullDown → MotionMultiplier | Decimal | 1.0 | 0.01..10.0 | Downward impulse scale. |
| OnlyInCombat → Mode → [NCP] → PullDown → OnTick | Integer | 5 | 1..9 | Air tick at which pull-down fires. |
| OnlyInCombat → Mode → [NCP] → PullDown → OnHurt | Toggle | true | — | Additional downward impulse when hurt. |
| OnlyInCombat → Mode → [NCP] → Boost | Toggleable Group | on | — | Constant horizontal speed boost per tick. |
| OnlyInCombat → Mode → [NCP] → Boost → InitialBoostMultiplier | Decimal | 1.0 | 0.01..10.0 | Scales the per-tick boost constant. |
| OnlyInCombat → Mode → [NCP] → Timer | Toggle | true | — | Requests 1.08× timer speed. |
| OnlyInCombat → Mode → [NCP] → DamageBoost | Toggle | true | — | Boosts speed when hurt. |
| OnlyInCombat → Mode → [NCP] → LowHop | Toggle | true | — | Reduces jump height to 0.4. |
| OnlyInCombat → Mode → [NCP] → AirStrafe | Toggle | true | — | Strafe correction while airborne. |
| OnlyInCombat → Mode → [Intave14] → Strafe | Toggleable Group | on | — | Strafe optimisation while sprinting. |
| OnlyInCombat → Mode → [Intave14] → Strafe → Strength | Decimal | 0.29 | 0.01..0.27 | Strafe correction strength. |
| OnlyInCombat → Mode → [Intave14] → AirBoost | Toggleable Group | on | — | Horizontal speed boost while ascending. |
| OnlyInCombat → Mode → [Intave14Fast] → Timer | Toggle | true | — | Applies a 1.002× timer speed boost. |
| OnlyInCombat → Mode → [BlocksMC] → RoundStrafeYaw | Toggle | false | — | Rounds movement yaw to the nearest 45°. |
| OnlyOnPotionEffect | Toggleable Group | on | — | When enabled, activates a separate speed mode only while a specific potion effect condition is met. |
| OnlyOnPotionEffect → PotionEffect | Mode Selector | Speed | — | Which potion effect condition to check: Speed (by amplifier level), Slowness (by amplifier level), or Both (combined movement multiplier). |
| OnlyOnPotionEffect → PotionEffect → [Speed] → LevelRange | Integer Range | 1..4 | 0..4 | Speed effect amplifier range that triggers activation (1 = Speed I, 2 = Speed II, etc.). |
| OnlyOnPotionEffect → PotionEffect → [Slowness] → LevelRange | Integer Range | 1..2 | 0..4 | Slowness amplifier range that triggers activation. |
| OnlyOnPotionEffect → PotionEffect → [Both] → PotionEffectsBoostRange | Decimal Range | 1.15..1.35 | 0.25..2.0 | Combined net movement multiplier range (Speed and Slowness together) that triggers activation. |
| OnlyOnPotionEffect → Mode | Mode Selector | Custom | — | Speed bypass mode used when the potion effect condition is met. Same options as the top-level Mode. |
| OnlyOnPotionEffect → Mode → [Custom] → HorizontalModification | Toggleable Group | on | — | (Potion) Horizontal acceleration and jump-off boost. |
| OnlyOnPotionEffect → Mode → [Custom] → HorizontalModification → HorizontalAcceleration | Decimal | 0.03 | -0.1..0.2 | Multiplies horizontal velocity by (1 + this value) every tick while moving. |
| OnlyOnPotionEffect → Mode → [Custom] → HorizontalModification → HorizontalJumpOff | Decimal | 0.14 | -0.5..1.0 | Multiplies horizontal velocity by (1 + this value) when jumping off the ground. |
| OnlyOnPotionEffect → Mode → [Custom] → HorizontalModification → TicksToBoostOff | Integer | 0 | 0..20 ticks | Delay in ticks before the jump-off boost fires. |
| OnlyOnPotionEffect → Mode → [Custom] → VerticalModification | Toggleable Group | off | — | (Potion) Jump height and vertical pull-down forces. |
| OnlyOnPotionEffect → Mode → [Custom] → VerticalModification → JumpHeight | Decimal | 0.42 | 0.0..3.0 | Vertical velocity when jumping. |
| OnlyOnPotionEffect → Mode → [Custom] → VerticalModification → Pulldown | Decimal | 0.0 | 0.0..1.0 | Downward force while moving upward. |
| OnlyOnPotionEffect → Mode → [Custom] → VerticalModification → PullDownDuringFall | Decimal | 0.0 | 0.0..1.0 | Downward force while falling. |
| OnlyOnPotionEffect → Mode → [Custom] → TimerSpeed | Decimal | 1.0 | 0.1..10.0 | Timer multiplier while moving. |
| OnlyOnPotionEffect → Mode → [Custom] → Strafe | Toggleable Group | on | — | (Potion) Strafe correction. |
| OnlyOnPotionEffect → Mode → [Custom] → Strafe → Strength | Decimal | 1.0 | 0.1..1.0 | Strafe correction strength. |
| OnlyOnPotionEffect → Mode → [Custom] → Strafe → CustomSpeed | Toggle | true | — | Force horizontal speed to the Speed value. |
| OnlyOnPotionEffect → Mode → [Custom] → Strafe → Speed | Decimal | 0.35 | 0.1..10.0 | Target speed (blocks/tick) when CustomSpeed is on. |
| OnlyOnPotionEffect → Mode → [Custom] → Strafe → VelocityTimeout | Integer | 0 | 0..20 ticks | Ticks to pause strafing after a knockback packet. |
| OnlyOnPotionEffect → Mode → [Custom] → Strafe → StrafeKnock | Toggle | true | — | Re-applies strafe direction after a knockback packet. |
| OnlyOnPotionEffect → Mode → [YPort] → Speed | Decimal | 0.4 | 0.1..1.0 | Horizontal speed applied after each jump. |
| OnlyOnPotionEffect → Mode → [PiercingAttack] → SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Swing animation visibility during piercing attacks. |
| OnlyOnPotionEffect → Mode → [PiercingAttack] → HoldTime | Integer Range | 1..1 | 1..20 ticks | Ticks to silently hold the piercing weapon. |
| OnlyOnPotionEffect → Mode → [PiercingAttack] → OnGround | Toggle | true | — | Only boost while on the ground. |
| OnlyOnPotionEffect → Mode → [PiercingAttack] → IgnoreHunger | Toggle | false | — | Boost even when hunger is low. |
| OnlyOnPotionEffect → Mode → [PiercingAttack] → WaitForCooldown | Toggle | true | — | Wait for the attack cooldown before re-attacking. |
| OnlyOnPotionEffect → Mode → [PiercingAttack] → MinimumDurability | Integer | 1 | 0..20 | Minimum weapon durability required. |
| OnlyOnPotionEffect → Mode → [HypixelBHop] → HorizontalAcceleration | Toggle | true | — | Horizontal speed boost per air tick. |
| OnlyOnPotionEffect → Mode → [HypixelBHop] → VerticalAcceleration | Toggle | true | — | Reduces vertical descent during early fall. |
| OnlyOnPotionEffect → Mode → [HypixelLowHop] → Glide | Toggle | true | — | Zeroes vertical velocity at air tick 7 when near the ground. |
| OnlyOnPotionEffect → Mode → [SentinelDamage] → Speed | Decimal | 0.5 | 0.1..5.0 | Strafe speed during the damage-boost phase. |
| OnlyOnPotionEffect → Mode → [SentinelDamage] → ReboostTicks | Integer | 30 | 10..50 | Ticks between boost packet cycles. |
| OnlyOnPotionEffect → Mode → [GrimCollide] → BoostSpeed | Decimal | 0.08 | 0.01..0.08 b/t | Speed boost per nearby entity. |
| OnlyOnPotionEffect → Mode → [GrimCollide] → ShrinkBox | Decimal | 0.5 | 0.1..2.0 | Entity detection radius in blocks. |
| OnlyOnPotionEffect → Mode → [NCP] → PullDown | Toggleable Group | on | — | Pull-down impulse at a specific air tick. |
| OnlyOnPotionEffect → Mode → [NCP] → PullDown → MotionMultiplier | Decimal | 1.0 | 0.01..10.0 | Downward impulse scale. |
| OnlyOnPotionEffect → Mode → [NCP] → PullDown → OnTick | Integer | 5 | 1..9 | Air tick at which pull-down fires. |
| OnlyOnPotionEffect → Mode → [NCP] → PullDown → OnHurt | Toggle | true | — | Additional downward impulse when hurt. |
| OnlyOnPotionEffect → Mode → [NCP] → Boost | Toggleable Group | on | — | Constant horizontal speed boost per tick. |
| OnlyOnPotionEffect → Mode → [NCP] → Boost → InitialBoostMultiplier | Decimal | 1.0 | 0.01..10.0 | Scales the per-tick boost constant. |
| OnlyOnPotionEffect → Mode → [NCP] → Timer | Toggle | true | — | Requests 1.08× timer speed. |
| OnlyOnPotionEffect → Mode → [NCP] → DamageBoost | Toggle | true | — | Boosts speed when hurt. |
| OnlyOnPotionEffect → Mode → [NCP] → LowHop | Toggle | true | — | Reduces jump height to 0.4. |
| OnlyOnPotionEffect → Mode → [NCP] → AirStrafe | Toggle | true | — | Strafe correction while airborne. |
| OnlyOnPotionEffect → Mode → [Intave14] → Strafe | Toggleable Group | on | — | Strafe optimisation while sprinting. |
| OnlyOnPotionEffect → Mode → [Intave14] → Strafe → Strength | Decimal | 0.29 | 0.01..0.27 | Strafe correction strength. |
| OnlyOnPotionEffect → Mode → [Intave14] → AirBoost | Toggleable Group | on | — | Horizontal speed boost while ascending. |
| OnlyOnPotionEffect → Mode → [Intave14Fast] → Timer | Toggle | true | — | Applies a 1.002× timer speed boost. |
| OnlyOnPotionEffect → Mode → [BlocksMC] → RoundStrafeYaw | Toggle | false | — | Rounds movement yaw to the nearest 45°. |
| YawOffset | Toggleable Group | on | — | Offsets the effective facing yaw to gain extra speed from the strafe movement bonus. |
| YawOffset → YawOffsetMode | Choice | Air | Ground, Air, Constant | When the offset is applied: Ground = on the ground only; Air = airborne while moving straight forward (applies a −45° offset); Constant = whenever moving in any direction. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/speed/ModuleSpeed.kt)*
