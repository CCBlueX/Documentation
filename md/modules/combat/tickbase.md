## TickBase

Buffer ticks to get early hits on an enemy.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Choice | default: PAST | options: Past, Future)
├── Call (Choice | default: GAME | options: Game, Player)
├── Range (Decimal Range | default: 2.5..4.0 | range: 0.0..8.0)
├── BalanceRecoverIncrement (Decimal | default: 1.0 | range: 0.0..2.0)
├── BalanceMaxValue (Integer | default: 20 | range: 0..200)
├── MaxTicksAtATime (Integer | default: 4 | range: 1..20 | ticks)
├── PauseOfFlag (Toggle | default: true)
├── Pause (Integer | default: 0 | range: 0..20 | ticks)
├── Cooldown (Integer | default: 0 | range: 0..100 | ticks)
├── ForceGround (Toggle | default: false)
├── Line (Color)
└── RequiresKillAura (Toggle | default: true)
```

### Settings Details

- **Mode** (Choice) — default: `PAST`; options: `Past`, `Future` — Past freezes player ticks then replays them; Future runs extra ticks ahead then freezes.
- **Call** (Choice) — default: `GAME`; options: `Game`, `Player` — Game runs a full game tick; Player only ticks the player entity.
- **Range** (Decimal Range) — default: `2.5` – `4.0`; range: `0.0` – `8.0` — Distance range to the target where tick-base activates (min = can tick into, max = won't activate beyond).
- **BalanceRecoverIncrement** (Decimal) — default: `1.0`; range: `0.0` – `2.0` — How many balance points are recovered each tick.
- **BalanceMaxValue** (Integer) — default: `20`; range: `0` – `200` — Maximum tick balance that can be accumulated.
- **MaxTicksAtATime** (Integer) — default: `4`; range: `1` – `20`; unit: ticks — Maximum number of ticks that can be shifted in a single burst.
- **PauseOfFlag** (Toggle) — default: `true` — Resets tick balance when a server position correction (flag) is received.
- **Pause** (Integer) — default: `0`; range: `0` – `20`; unit: ticks — Additional ticks to freeze after the tick-base burst.
- **Cooldown** (Integer) — default: `0`; range: `0` – `100`; unit: ticks — Ticks to wait after a tick-base burst before allowing another.
- **ForceGround** (Toggle) — default: `false` — Only selects tick positions where the player is on the ground.
- **Line** (Color) — Color of the line rendered along the predicted tick path.
- **RequiresKillAura** (Toggle) — default: `true` — Only activates when KillAura is running and ready to attack.

### Screenshots

*Screenshots for TickBase will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleTickBase.kt)*
