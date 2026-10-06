## TickBase

TickBase is a combat module that simulates your future player positions tick-by-tick and, when an enemy enters the configured range, fires a burst of extra ticks to effectively move your client forward in time. The result is that your character reaches an optimal attack position earlier than normal, landing hits sooner than the server would otherwise allow. It works best alongside [KillAura](/docs/modules/combat/killaura), which is why **RequiresKillAura** is on by default — TickBase will only activate when KillAura is running and ready to strike at the predicted tick.

A balance system prevents TickBase from firing without limit. Each activation drains balance, which slowly refills each game tick at a rate set by **BalanceRecoverIncrement** up to the cap in **BalanceMaxValue**. If the server sends a position correction (commonly called a flag), **PauseOfFlag** immediately zeroes the balance, pausing further activations until it recovers. You can further throttle activations with the **Cooldown** setting and limit how many ticks fire at once with **MaxTicksAtATime**.

TickBase automatically disables itself while you are riding a vehicle or while [Blink](/docs/modules/player/blink) is active to avoid conflicts. If you set the **Line** colour with a visible alpha, an in-world line traces the simulated tick path so you can see exactly where the module is projecting your position.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Past | — | How extra ticks are executed. `Past` fires all buffered ticks at once and then pauses normal ticking to compensate. `Future` fires ticks one at a time, stopping early if [KillAura](/docs/modules/combat/killaura) is no longer ready to hit. |
| Call | Choice | Game | — | Scope of each extra tick. `Game` runs a full game tick; `Player` runs only the player tick (lighter, and the legacy default behaviour). |
| Range | Decimal Range | 3.0..5.0 | 0.0..8.0 | Distance window that triggers TickBase. The lower bound is the minimum distance to a target before activation begins; the upper bound is the maximum distance at which it will trigger at all. |
| BalanceRecoverIncrement | Decimal | 1.0 | 0.0..2.0 | How much tick balance is restored each game tick. Higher values allow TickBase to fire more frequently. |
| BalanceMaxValue | Integer | 20 | 0..200 | Maximum tick balance that can accumulate, capping how many extra ticks can be stored between activations. |
| MaxTicksAtATime | Integer | 2 | 1..20 | Maximum number of extra ticks that can be fired in a single activation. |
| PauseOfFlag | Toggle | true | — | When enabled, resets the tick balance to zero upon receiving a server-side position correction (flag), halting further activations until balance recovers naturally. |
| Pause | Integer | 2 | 0..20 | Additional ticks to wait after an activation before normal ticking resumes, giving the server time to process the burst. |
| Cooldown | Integer | 0 | 0..100 | Minimum number of ticks to wait between TickBase activations. |
| ForceGround | Toggle | false | — | When enabled, TickBase only considers tick snapshots where the player is on the ground, which can help ensure critical hits land. |
| Line | Color | — | — | Colour of the in-world line that visualises the simulated tick path. Set alpha to 0 to hide the line entirely. |
| RequiresKillAura | Toggle | true | — | When enabled, TickBase only activates if [KillAura](/docs/modules/combat/killaura) is running and its clicker is predicted to fire at the selected tick. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleTickBase.kt)*
