## AutoWindCharge

AutoWindCharge automatically detonates a wind charge beneath you to launch you into the air every time you land, as long as you're holding the jump key. It's a movement aid for the 1.21+ wind charge item: instead of manually timing throws, the module throws the charge and times your jump for you so you keep bouncing high off the ground, using one charge per bounce.

Each tick the module checks that you're holding jump and aren't flying, swimming, or in liquid. While you're on the ground and the wind charge isn't on cooldown, it throws the charge at your feet and holds back your jump for one tick, so you jump right as the charge bursts below you and the jump and the knockback add up. It looks for a wind charge in your hotbar or offhand and uses it from there, so the item never has to be in your main hand.

By default the boost aims straight down (pitch 90) to throw you upward. Holding the **HorizontalBoost** key instead aims at a pitch picked from the configured **Pitch** range and points opposite your movement input, giving you a flatter, more horizontal launch for covering distance. When **Rotate** is on, the module already starts turning toward the aim point while you fall, shortly before landing, and only fires once your rotation is close enough (within 1°). If the turn isn't finished after 10 ticks on the ground, you jump without a charge.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| HorizontalBoost | Toggleable Group | on | — | When its key is held, aims the wind charge at the set pitch (opposite your input direction) for a flatter, horizontal launch instead of a straight-up boost. |
| HorizontalBoost → Pitch | Decimal Range | 70.0..70.0 | 0.0..90.0 | Aim pitch used while horizontal boosting, picked at random from this range. Lower values launch you more horizontally; higher values closer to vertical. |
| HorizontalBoost → Key | Key | — | — | Hold this key to trigger a horizontal boost. Bound to Left Control by default. |
| Rotate | Toggleable Group | on | — | Turns toward the boost direction before firing and only uses the charge once aim is within 1° of the target. |
| Rotate → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| CombatPauseTime | Integer | 0 | 0..40 | Ticks to pause combat-related actions while rotating to boost. 0 disables the pause. |
| SlotResetDelay | Integer Range | 0..0 | 0..40 | Random delay (in ticks, picked from this range) before switching back from the wind charge slot after using it. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoWindCharge.kt)*
