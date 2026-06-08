## AutoTrap

AutoTrap is a combat-utility module that punishes nearby enemies by placing hazardous blocks underneath them — either setting them on fire (lava or flint and steel) or trapping them in cobwebs. It's most useful in PvP situations where you want to lock down or chip away at an opponent without relying solely on your sword: webs slow and pin a target so they can't escape your KillAura, while ignition deals damage over time and pressures players who are low on health or out of food.

Rather than naively spamming blocks, AutoTrap predicts where a jumping or falling enemy is about to land and lays the trap there. It runs a [player movement simulation](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/traps/traps/TrapPlayerSimulation.kt#L91-L133) over the next ~25 ticks, only committing once it has enough consistent evidence (low landing-position variance) that the prediction is reliable. The module first tries the [web planner, then falls back to ignition](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/traps/ModuleAutoTrap.kt#L88-L107), picking placement faces that overlap the predicted target box.

To avoid wasting your attack rhythm, placements are deliberately timed: when KillAura is mid-combat, AutoTrap [waits for a "propitious moment"](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/traps/ModuleAutoTrap.kt#L159-L173) — slotting the block in during recovery so it doesn't cancel a charged or critical hit. After a successful placement it pauses for the configured Delay before acting again. Note that ignition is skipped for targets already on fire, and both trap types require the appropriate items (cobweb, or lava bucket / flint and steel) in your hotbar or offhand.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal Range | 3.0..4.5 | 2.0..6.0 | Distance window (in blocks) used to acquire targets for trapping. |
| Delay | Integer | 20 | 0..400 | Cooldown in ticks to wait after a successful placement before trapping again. |
| IgnoreOpenInventory | Toggle | true | — | When enabled, AutoTrap keeps working while a container/inventory screen is open. Disable it to pause trapping (and to consider the open inventory) while a screen is up. |
| Ignite | Toggleable Group | on | — | Enables the fire trap, placing lava or flint and steel at targets to set them ablaze. Targets already on fire are skipped. |
| AutoWeb | Toggleable Group | on | — | Enables the cobweb trap, placing cobwebs at targets to slow and pin them in place. |
| Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/traps/ModuleAutoTrap.kt)*
