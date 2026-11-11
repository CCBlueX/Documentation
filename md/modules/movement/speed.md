## Speed

Speed makes you run faster than normal sprinting. Pick the mode made for the anti-cheat on your server. LegitHop is a careful bunny hop that works on many servers, and Custom lets you set every value yourself.

OnlyInCombat and OnlyOnPotionEffect each have their own mode. When OnlyInCombat is on, its mode replaces the main one while you fight. OnlyOnPotionEffect does the same while you have a Speed or Slowness effect.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | LegitHop | LegitHop, Custom, YPort, PiercingAttack, Verus-b3882, HypixelBHop, HypixelLowHop, Spartan-4.0.4.3, Spartan-4.0.4.3-FastFall, CubeCraft-2024-06-30, Vulcan-2.8.6, Vulcan-2.8.8, Vulcan-2.8.6-Ground, Grim-2.3.73, NCP-2024-08-31, Intave-14, Intave-14-Fast, HylexLowHop, HylexGround, BlocksMC, Matrix-7 | How you go faster. Modes not listed below have no settings. |
| Mode → [Custom] → HorizontalModification | Toggleable Group | On |  | Change your speed on the ground and when you jump. |
| Mode → [Custom] → HorizontalModification → HorizontalAcceleration | Decimal | 0.0 | -0.1..0.2 | Extra speed added all the time while you move. |
| Mode → [Custom] → HorizontalModification → HorizontalJumpOff | Decimal | 0.0 | -0.5..1.0 | Extra speed added when you jump. |
| Mode → [Custom] → HorizontalModification → TicksToBoostOff | Integer | 0 | 0..20 ticks | Ticks (20 per second) to wait after the jump before that boost. |
| Mode → [Custom] → VerticalModification | Toggleable Group | On |  | Change how you jump and fall. |
| Mode → [Custom] → VerticalModification → JumpHeight | Decimal | 0.42 | 0.0..3.0 | How high you jump. A normal jump is 0.42. |
| Mode → [Custom] → VerticalModification → Pulldown | Decimal | 0.0 | 0.0..1.0 | Pull you down while you go up. |
| Mode → [Custom] → VerticalModification → PullDownDuringFall | Decimal | 0.0 | 0.0..1.0 | Pull you down while you fall. |
| Mode → [Custom] → TimerSpeed | Decimal | 1.0 | 0.1..10.0 | How fast the game runs for you while you move. Above 1 is faster. |
| Mode → [Custom] → Strafe | Toggleable Group | On |  | Let you change direction in the air without losing speed. |
| Mode → [Custom] → Strafe → Strength | Decimal | 1.0 | 0.1..1.0 | How strong the steering is. |
| Mode → [Custom] → Strafe → CustomSpeed | Toggle | false |  | Always move at the Speed below. |
| Mode → [Custom] → Strafe → Speed | Decimal | 1.0 | 0.1..10.0 | The speed used when CustomSpeed is on. |
| Mode → [Custom] → Strafe → VelocityTimeout | Integer | 0 | 0..20 ticks | Ticks to stop steering after you get knocked back. |
| Mode → [Custom] → Strafe → StrafeKnock | Toggle | false |  | Keep steering when you get knocked back. |
| Mode → [YPort] → Speed | Decimal | 0.4 | 0.1..1.0 | How fast you go after each jump. |
| Mode → [PiercingAttack] → HoldTime | Integer Range | 1..1 | 1..20 ticks | How long to hold the spear before switching back. |
| Mode → [PiercingAttack] → OnGround | Toggle | true |  | Only boost while you stand on the ground. |
| Mode → [PiercingAttack] → IgnoreHunger | Toggle | false |  | Boost even when you are too hungry to sprint. |
| Mode → [PiercingAttack] → WaitForCooldown | Toggle | true |  | Wait until the weapon is fully charged before the next boost. |
| Mode → [PiercingAttack] → MinimumDurability | Integer | 1 | 0..20 | Don't use a weapon with less durability than this. |
| Mode → [HypixelBHop] → HorizontalAcceleration | Toggle | true |  | Gain a bit of speed in the air. |
| Mode → [HypixelBHop] → VerticalAcceleration | Toggle | true |  | Fall a bit slower at the start of a fall. |
| Mode → [HypixelLowHop] → Glide | Toggle | false |  | Stop falling for a moment when you are close to the ground. |
| Mode → [CubeCraft-2024-06-30] → Speed | Decimal | 0.5 | 0.1..5.0 | How fast you go during the boost. |
| Mode → [CubeCraft-2024-06-30] → ReboostTicks | Integer | 30 | 10..50 | Ticks between boosts. |
| Mode → [Grim-2.3.73] → BoostSpeed | Decimal | 0.08 | 0.01..0.08 b/t | Speed you gain for each player or mob you touch. |
| Mode → [Grim-2.3.73] → ShrinkBox | Decimal | 0.5 | 0.1..2.0 | How close a player or mob must be to count. |
| Mode → [NCP-2024-08-31] → PullDown | Toggleable Group | On |  | Pull you down during the jump so it is lower. |
| Mode → [NCP-2024-08-31] → PullDown → MotionMultiplier | Decimal | 1.0 | 0.01..10.0 | How strong the pull is. |
| Mode → [NCP-2024-08-31] → PullDown → OnTick | Integer | 5 | 1..9 | How many ticks after the jump it pulls. |
| Mode → [NCP-2024-08-31] → PullDown → OnHurt | Toggle | true |  | Also pull you down when you get hurt. |
| Mode → [NCP-2024-08-31] → Boost | Toggleable Group | On |  | Add a little speed while you move. |
| Mode → [NCP-2024-08-31] → Boost → InitialBoostMultiplier | Decimal | 1.0 | 0.01..10.0 | How strong that boost is. |
| Mode → [NCP-2024-08-31] → Timer | Toggle | true |  | Run the game a little faster for you. |
| Mode → [NCP-2024-08-31] → DamageBoost | Toggle | true |  | Go faster when you get hurt. |
| Mode → [NCP-2024-08-31] → LowHop | Toggle | true |  | Make your jumps lower. |
| Mode → [NCP-2024-08-31] → AirStrafe | Toggle | true |  | Let you steer in the air. |
| Mode → [Intave-14] → Strafe | Toggleable Group | On |  | Let you steer without losing speed. |
| Mode → [Intave-14] → Strafe → Strength | Decimal | 0.27 | 0.01..0.27 | How strong the steering is. |
| Mode → [Intave-14] → AirBoost | Toggleable Group | On |  | Gain a bit of speed while you go up. |
| Mode → [Intave-14-Fast] → Timer | Toggle | true |  | Run the game a tiny bit faster for you. |
| Mode → [BlocksMC] → RoundStrafeYaw | Toggle | false |  | Only steer in 8 directions. |
| Not | Multi-Select | [DuringScaffold] | WhileUsingItem, DuringScaffold, WhileSneaking, IsFallFlying, IsInLiquid | Pause Speed while one of these is true. DuringScaffold also covers [Fly](/docs/modules/movement/fly). |
| AvoidEdgeBump | Toggle | true |  | Wait with a jump if you would bump into the corner of a block. |
| OnlyInCombat | Toggleable Group | Off |  | Use a different mode while you fight. |
| OnlyInCombat → Mode | Mode Selector | LegitHop | Same as Mode | The mode used while you fight. It has the same settings as the main Mode. |
| OnlyOnPotionEffect | Toggleable Group | Off |  | Use a different mode while you have a Speed or Slowness effect. |
| OnlyOnPotionEffect → PotionEffect | Mode Selector | Speed | Speed, Slowness, Both | Which effect to check. |
| OnlyOnPotionEffect → PotionEffect → [Speed] → LevelRange | Integer Range | 1..2 | 0..4 | Speed levels that count (1 is Speed I). |
| OnlyOnPotionEffect → PotionEffect → [Slowness] → LevelRange | Integer Range | 1..2 | 0..4 | Slowness levels that count. |
| OnlyOnPotionEffect → PotionEffect → [Both] → PotionEffectsBoostRange | Decimal Range | 1.15..1.35 | 0.25..2.0 | How much faster both effects together make you, for example 1.2 means 20% faster. |
| OnlyOnPotionEffect → Mode | Mode Selector | LegitHop | Same as Mode | The mode used while the effect is on you. It has the same settings as the main Mode. |
| YawOffset | Toggleable Group | Off |  | Turn your body sideways while you run, which gives a little more speed. |
| YawOffset → YawOffsetMode | Mode Selector | Air | Ground, Air, Constant | When to turn: on the ground, in the air, or all the time. |
| YawOffset → Rotations | Setting Group |  |  | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/speed/ModuleSpeed.kt)*
