## TimerRange

Accelerates the game time when being within the range of an enemy.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Chance (Integer | default: 100 | range: 0..100 | %)
├── TimerBalanceLimit (Decimal | default: 20.0 | range: 0.0..50.0)
├── NormalSpeed (Decimal | default: 0.9 | range: 0.1..10.0)
├── InRangeSpeed (Decimal | default: 0.95 | range: 0.1..10.0)
├── BalanceLimitSpeed (Decimal | default: 0.99 | range: 0.1..1.0)
├── BoostTimer (Decimal | default: 2.0 | range: 0.1..10.0)
├── BalanceRecoveryIncrement (Decimal | default: 1.0 | range: 1.0..10.0)
├── DistanceToSpeedUp (Decimal | default: 3.5 | range: 0.0..10.0)
├── DistanceToPause (Decimal | default: 3.0 | range: 0.0..10.0)
├── DistanceToStartWorking (Decimal | default: 100.0 | range: 0.0..500.0)
├── PauseOnFlag (Toggle | default: true)
├── OnlyOnGround (Toggle | default: false)
└── RequiresKillAura (Toggle | default: true)
```

### Settings Details

- **Chance** (Integer) — default: `100`; range: `0` – `100`; unit: % — Probability that the timer speed change is applied each tick.
- **TimerBalanceLimit** (Decimal) — default: `20.0`; range: `0.0` – `50.0` — Maximum timer balance before speed-up is throttled.
- **NormalSpeed** (Decimal) — default: `0.9`; range: `0.1` – `10.0` — Timer speed when an enemy is in working range but not yet close enough to boost.
- **InRangeSpeed** (Decimal) — default: `0.95`; range: `0.1` – `10.0` — Timer speed applied when close to an enemy and the balance limit has been reached.
- **BalanceLimitSpeed** (Decimal) — default: `0.99`; range: `0.1` – `1.0` — Slow-down timer speed applied when the balance drops below the limit.
- **BoostTimer** (Decimal) — default: `2.0`; range: `0.1` – `10.0` — Timer speed multiplier applied when within speed-up distance and balance is available.
- **BalanceRecoveryIncrement** (Decimal) — default: `1.0`; range: `1.0` – `10.0` — Divisor for how quickly the timer balance recovers each tick.
- **DistanceToSpeedUp** (Decimal) — default: `3.5`; range: `0.0` – `10.0` — Distance to the enemy at which the boost timer speed activates.
- **DistanceToPause** (Decimal) — default: `3.0`; range: `0.0` – `10.0` — Distance to the enemy at which timer returns to normal (1.0×) speed.
- **DistanceToStartWorking** (Decimal) — default: `100.0`; range: `0.0` – `500.0` — Maximum distance to any enemy for the module to be active at all.
- **PauseOnFlag** (Toggle) — default: `true` — Resets the timer balance when a server position correction is received.
- **OnlyOnGround** (Toggle) — default: `false` — Only modifies timer speed while the player is on the ground.
- **RequiresKillAura** (Toggle) — default: `true` — Only activates when KillAura is running and has a target.

### Screenshots

*Screenshots for TimerRange will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleTimerRange.kt)*
