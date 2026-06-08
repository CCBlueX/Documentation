## AutoPearl

AutoPearl watches for ender pearls thrown by other players and automatically throws your own pearl to follow them. When an enemy pearls away, the module simulates where their pearl will land, then calculates the throw angle needed to land your pearl at that same spot so you arrive at their destination too — useful for chasing opponents who try to escape with pearls.

It reacts to the pearl-spawn packet the moment an enemy's pearl appears, recreates the projectile, and [runs a trajectory simulation](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoPearl.kt#L221-L237) to find its landing point. It then asks the [projectile angle calculator](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoPearl.kt#L173-L186) for the rotation that lands your pearl there. In **Trigger** mode it responds to any pearl from a player who should be attacked (and ownerless pearls), while in **Target** mode it only follows the pearl of your current KillAura target.

Before throwing, the module can [check several limits](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoPearl.kt#L188-L219): how far off your crosshair the incoming pearl is, how close the landing spot is to you, and how accurately your own simulated throw would reach that spot. When rotations are enabled it waits until your aim is within one degree of the target before releasing the pearl from your hotbar or offhand.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Trigger | Trigger, Target | Which pearls to follow. **Trigger**: any pearl thrown by a player marked as a target (and ownerless pearls). **Target**: only the pearl thrown by your current KillAura target. |
| Rotate | Toggleable Group | on | — | When enabled, aims toward the calculated throw angle and only releases once your server-side aim is within 1° of it. |
| Rotate → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Limits | Toggleable Group | on | — | When enabled, applies the angle, distance, and accuracy checks below before throwing. |
| Limits → Angle | Integer | 180 | 0..180° | Maximum angle between your crosshair and the incoming enemy pearl for it to be considered. Larger values react to pearls further from where you're looking. |
| Limits → MinDistance | Decimal | 8.0 | 0.0..10.0m | Minimum distance the pearl's landing spot must be from you; closer destinations are ignored so you don't pearl onto yourself. |
| Limits → DestinationDistance | Decimal | 8.0 | 0.0..30.0m | Maximum allowed gap between the enemy's landing spot and where your own simulated throw would land; throws that would miss by more than this are skipped. |
| CombatPauseTime | Integer | 0 | 0..40 ticks | How long to pause combat (e.g. KillAura) while AutoPearl is aiming/throwing, preventing aim conflicts. |
| SlotResetDelay | Integer Range | 0..0 | 0..40 ticks | Random delay (in the given range) before the hotbar slot is reset after the pearl is used. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoPearl.kt)*
