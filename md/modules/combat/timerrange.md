## TimerRange

TimerRange dynamically adjusts the game's internal tick speed based on how close you are to an enemy. Unlike the flat [Timer](/docs/modules/world/timer) module which runs at a constant speed, TimerRange is reactive: it idles at a slightly reduced speed when no enemies are nearby, ramps up to a strong boost when you close in on a target, and pauses entirely if you get very close. This lets you land hits faster during the critical moments of a fight while spending most of your time at a less suspicious speed.

A built-in balance system tracks the "debt" accumulated from running the timer above normal. Once that debt reaches the `TimerBalanceLimit`, the module automatically throttles back to `BalanceLimitSpeed` and waits for it to recover, preventing extended high-speed periods that could trigger anti-cheat systems. If `PauseOnFlag` is on, any server-issued position correction resets the balance counter to its maximum, giving the module time to cool down naturally after being flagged.

By default, `RequiresKillAura` is enabled, meaning TimerRange only activates when [KillAura](/docs/modules/combat/killaura) is running and has an active target locked. This keeps the boost tightly coupled to actual combat engagement rather than firing whenever any player happens to wander nearby.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Chance | Decimal | 100.0 | 0.0..100.0 % | Probability per tick that the timer boost is applied when an enemy is in range. Values below 100 make the boost intermittent, which can appear more natural to anti-cheat. |
| TimerBalanceLimit | Decimal | 20.0 | 0.0..50.0 | How much timer-speed "debt" can accumulate before the module throttles down to `BalanceLimitSpeed`. Higher values allow longer boost windows before the cooldown phase begins. |
| NormalSpeed | Decimal | 0.9 | 0.1..10.0 | Timer multiplier applied when an enemy is detected within `DistanceToStartWorking` but still outside `DistanceToSpeedUp`. The default of 0.9× slightly slows the game in the approach phase. |
| InRangeSpeed | Decimal | 0.95 | 0.1..10.0 | Timer multiplier used once the balance limit has been exhausted during a boost sequence — a reduced in-combat speed to help the balance recover while still providing a minor edge. |
| BalanceLimitSpeed | Decimal | 0.99 | 0.1..1.0 | Timer multiplier applied while the internal balance counter is below `TimerBalanceLimit`. Keeps the game running just under normal speed to let the balance recover gradually. |
| BoostTimer | Decimal | 2.0 | 0.1..10.0 | Timer multiplier applied when an enemy is within `DistanceToSpeedUp` and the balance has not yet been exhausted. This is the main combat-speed boost. |
| BalanceRecoveryIncrement | Decimal | 1.0 | 1.0..10.0 | Controls how quickly the internal balance counter recovers when the timer is at or below normal. Higher values speed up recovery, allowing more frequent boost windows. |
| DistanceToSpeedUp | Decimal | 3.5 | 0.0..10.0 | Distance (in blocks) at which the full `BoostTimer` speed activates. Enemies closer than this value trigger the boost. |
| DistanceToPause | Decimal | 3.0 | 0.0..10.0 | Distance (in blocks) below which the timer resets to exactly 1.0× regardless of other settings. Prevents over-speeding at point-blank range. |
| DistanceToStartWorking | Decimal | 100.0 | 0.0..500.0 | Maximum detection radius (in blocks). TimerRange has no effect at all if the nearest enemy is farther away than this value. |
| PauseOnFlag | Toggle | true | — | When enabled, resets the balance timer to its maximum upon receiving a server position-correction packet, pausing further boosts and reducing the chance of a follow-up flag. |
| OnlyOnGround | Toggle | false | — | When enabled, the module only applies timer changes while you are standing on solid ground. |
| RequiresKillAura | Toggle | true | — | When enabled, TimerRange only activates while [KillAura](/docs/modules/combat/killaura) is running and has an active target. Disabling this allows TimerRange to operate independently. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleTimerRange.kt)*
