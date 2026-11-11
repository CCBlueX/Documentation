## Timer

Timer makes the game run faster or slower for you. Above 1.0 you move and act faster, below 1.0 slower. Many servers notice a fast timer, so use small values.

Boost mode runs slow while you stand still and fast while you move, so it evens out over time. It goes back to normal speed while you fight.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Classic | Classic, Pulse, Boost | Classic keeps one speed. Pulse switches between slow and fast. Boost saves up time while you stand and uses it when you move. |
| Mode → [Classic] → Speed | Decimal | 2.0 | 0.1..20.0 | Game speed. |
| Mode → [Pulse] → NormalSpeed | Decimal | 0.5 | 0.1..20.0 | Speed in the slow part. |
| Mode → [Pulse] → NormalSpeedTicks | Integer | 20 | 1..500 ticks | How long the slow part lasts (20 ticks per second). |
| Mode → [Pulse] → BoostSpeed | Decimal | 2.0 | 0.1..20.0 | Speed in the fast part. |
| Mode → [Pulse] → BoostSpeedTicks | Integer | 20 | 1..500 ticks | How long the fast part lasts. |
| Mode → [Pulse] → OnMove | Toggle | false | | Only switches while you move. |
| Mode → [Boost] → BoostSpeed | Decimal | 1.3 | 0.1..20.0 | Speed while you move. |
| Mode → [Boost] → SlowSpeed | Decimal | 0.6 | 0.1..20.0 | Speed while you stand still. |
| Mode → [Boost] → NormalizeDuringCombat | Toggle | true | | Uses normal speed while you fight. |
| Mode → [Boost] → Balance | Integer Range | 0..20 | -100..200 ticks | How much time it can save up and use. Below 0 lets it use more time than it saved. |
| Mode → [Boost] → ResetBalanceOnFlag | Toggle | true | | Clears the saved time when the server pulls you back. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleTimer.kt)*
