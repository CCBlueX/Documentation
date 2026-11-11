## AutoPearl

AutoPearl follows enemies who throw an ender pearl to get away. When an enemy throws one, it works out where the pearl will land and throws your own pearl to the same spot. You need an ender pearl in your hotbar or offhand.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Trigger | Trigger, Target | Which pearls to follow. Trigger follows the pearl of any enemy. Target only follows the pearl of your [KillAura](/docs/modules/combat/killaura) target. |
| Rotate | Toggleable Group | On | | Turns you to aim the pearl and only throws when your aim is right. |
| Rotate → Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Limits | Toggleable Group | On | | Uses the checks below before throwing. |
| Limits → Angle | Integer | 180 | 0..180 ° | How far away from where you look the enemy's pearl can be. 180 means anywhere. |
| Limits → MinDistance | Decimal | 8.0 | 0.0..10.0 m | Does not follow pearls that land closer to you than this. |
| Limits → DestinationDistance | Decimal | 8.0 | 0.0..30.0 m | Does not throw if your pearl would land further than this from the enemy's pearl. |
| CombatPauseTime | Integer | 0 | 0..40 ticks | How long to pause fighting modules like KillAura while aiming the pearl, in ticks (20 per second). |
| SlotResetDelay | Integer Range | 0..0 | 0..40 ticks | How long to wait after throwing before switching back to your old item. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoPearl.kt)*
