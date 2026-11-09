## Timer

Timer adjusts the speed at which the entire game runs on your client. A multiplier above 1.0 makes everything tick faster — you move, swing, and regenerate more quickly — while a value below 1.0 slows everything down. It is commonly used to cover ground faster, to farm more efficiently, or to gain an edge in combat timing.

Three modes are available to suit different needs. **Classic** applies a single, constant speed multiplier for as long as the module is active — straightforward but easy for anti-cheat systems to detect. **Pulse** automatically alternates between a slow phase and a fast phase on a configurable tick schedule, creating a more irregular pattern. **Boost** is the most nuanced option: it builds up the client's shared timer balance while you are standing still (running at a reduced speed), then spends that balance as a speed burst when you start moving, so the time averages out more naturally over the long run. The balance is shared with other modules such as [TickBase](/docs/modules/combat/tickbase).

Boost mode includes several safeguards to keep it practical in combat. The `NormalizeDuringCombat` option resets the timer to 1× speed while you are fighting so that combat modules such as [KillAura](/docs/modules/combat/killaura) or [CrystalAura](/docs/modules/combat/crystalaura) are not disrupted. The `Balance` range sets how far the balance may be spent and built up: speeding up may spend it down to the start of the range, which can be below 0 for anticheats that let the client run ahead, and slowing down stops once the end is reached. `ResetBalanceOnFlag` clears the balance when the server sends a position correction.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Classic | — | Selects which timer mode to use: Classic (constant speed), Pulse (alternating speeds), or Boost (movement-based credit system). |
| Mode → [Classic] → Speed | Decimal | 1.5 | 0.1–20.0 | Constant game speed multiplier. Values above 1.0 make the game run faster; values below 1.0 slow it down. |
| Mode → [Pulse] → NormalSpeed | Decimal | 0.5 | 0.1–20.0 | Speed multiplier applied during the slow phase between boosts. |
| Mode → [Pulse] → NormalSpeedTicks | Integer | 20 | 1–500 ticks | How long the slow phase lasts before switching to the boost phase. |
| Mode → [Pulse] → BoostSpeed | Decimal | 2.0 | 0.1–20.0 | Speed multiplier applied during the fast phase. |
| Mode → [Pulse] → BoostSpeedTicks | Integer | 20 | 1–500 ticks | How long the fast phase lasts before switching back to the slow phase. |
| Mode → [Pulse] → OnMove | Toggle | false | — | When enabled, the pulse cycle only progresses while the player is moving; it pauses while standing still. |
| Mode → [Boost] → BoostSpeed | Decimal | 1.3 | 0.1–20.0 | Speed multiplier applied when spending the timer balance while moving. |
| Mode → [Boost] → SlowSpeed | Decimal | 0.6 | 0.1–20.0 | Speed multiplier applied while standing still to build up the timer balance. |
| Mode → [Boost] → NormalizeDuringCombat | Toggle | true | — | Reverts the timer to 1.0× speed while in combat to avoid disrupting combat module timing. |
| Mode → [Boost] → Balance | Integer Range | 0–20 | -100–200 ticks | Range of the timer balance Boost works within. Speeding up may spend the balance down to the start (below 0 lets the client run ahead of the server); slowing down stops at the end. |
| Mode → [Boost] → ResetBalanceOnFlag | Toggle | true | — | Clears the timer balance when the server sends a position correction (flag). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleTimer.kt)*
