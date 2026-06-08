## AutoWindCharge

AutoWindCharge automatically detonates a wind charge beneath you to launch you into the air the moment you'd otherwise land, as long as you're holding the jump key. It's a movement aid for the 1.21+ wind charge item: instead of manually timing throws, the module watches your fall and fires at the ideal moment so you keep bouncing higher off the ground.

Each tick the module checks that you're holding jump and aren't flying, swimming, or in liquid, then predicts where you'll land. Using a [7-tick look-ahead](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoWindCharge.kt#L61-L75) — described in the source as "the perfect time to use a wind charge before hitting the ground" — it only acts once a collision is imminent. It looks for a wind charge in your hotbar or offhand and uses it from there, so the item never has to be in your main hand.

By default the boost aims straight down (pitch 90) to throw you upward. Holding the **HorizontalBoost** key instead aims at the configured pitch and points opposite your movement input, giving you a flatter, more horizontal launch for covering distance. When **Rotate** is on, the module smoothly turns toward the aim point first and only fires [once your rotation is close enough](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoWindCharge.kt#L88-L110) (within 1°).

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| HorizontalBoost | Toggleable Group | on | — | When its key is held, aims the wind charge at the set pitch (opposite your input direction) for a flatter, horizontal launch instead of a straight-up boost. |
| HorizontalBoost → Pitch | Decimal | 70.0 | 0.0..90.0 | Aim pitch used while horizontal boosting. Lower values launch you more horizontally; higher values closer to vertical. |
| HorizontalBoost → Key | Key | — | — | Hold this key to trigger a horizontal boost. Bound to Left Control by default. |
| Rotate | Toggleable Group | on | — | Turns toward the boost direction before firing and only uses the charge once aim is within 1° of the target. |
| Rotate → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| CombatPauseTime | Integer | 0 | 0..40 | Ticks to pause combat-related actions while rotating to boost. 0 disables the pause. |
| SlotResetDelay | Integer Range | 0..0 | 0..40 | Random delay (in ticks, picked from this range) before switching back from the wind charge slot after using it. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoWindCharge.kt)*
