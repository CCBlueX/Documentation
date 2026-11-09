## TickBase

TickBase is a combat module that simulates your future player positions tick-by-tick and, when an enemy enters the configured range, fires a burst of extra ticks to effectively move your client forward in time. The result is that your character reaches an optimal attack position earlier than normal, landing hits sooner than the server would otherwise allow. It works best alongside [KillAura](/docs/modules/combat/killaura), which is why **RequiresKillAura** is on by default — TickBase will only activate when KillAura is running and ready to strike at the predicted tick.

With the `Timer` mode, TickBase speeds up the game timer instead of bursting ticks while you are near an enemy.

TickBase spends the client's shared timer balance: the number of ticks your client is behind the time the server saw pass. Held back ticks and a timer below 1× build it up, extra ticks and a timer above 1× spend it, no matter which module caused them (for example [Timer](/docs/modules/world/timer)). The **Balance** group sets the range within which TickBase may spend it, and the balance is cleared when the server sends a position correction (commonly called a flag) unless you turn off **ResetBalanceOnFlag**. You can further throttle activations with the **Cooldown** setting and limit how many ticks fire at once with **MaxTicksAtATime**.

TickBase automatically disables itself while you are riding a vehicle or while [Blink](/docs/modules/player/blink) is active to avoid conflicts. If you set the **Line** colour with a visible alpha, an in-world line traces the simulated tick path so you can see exactly where the module is projecting your position.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | HoldFirst | HoldFirst \| BurstFirst \| Timer | How TickBase spends the balance. `HoldFirst` (formerly `Past`) fires all buffered ticks at once and then pauses normal ticking to compensate. `BurstFirst` (formerly `Future`) fires ticks one at a time, stopping early if [KillAura](/docs/modules/combat/killaura) is no longer ready to hit. `Timer` speeds up the game timer near an enemy. Configs using the old names keep working. |
| Call | Choice | Game | — | Scope of each extra tick. `Game` runs a full game tick; `Player` runs only the player tick (lighter, and the legacy default behaviour). |
| Range | Decimal Range | 3.0..5.0 | 0.0..8.0 | Distance window that triggers TickBase. The lower bound is the minimum distance to a target before activation begins; the upper bound is the maximum distance at which it will trigger at all. |
| Balance | Setting Group | — | — | Limits how TickBase spends the shared timer balance. |
| Balance → Range | Integer Range | — | — | Range of the timer balance (in ticks) within which TickBase may spend it. |
| Balance → ResetBalanceOnFlag | Toggle | true | — | Clears the timer balance when the server sends a position correction (flag) while TickBase is running. |
| MaxTicksAtATime | Integer | 2 | 1..20 | Maximum number of extra ticks that can be fired in a single activation. |
| Pause | Integer | 2 | 0..20 | Additional ticks to wait after an activation before normal ticking resumes, giving the server time to process the burst. |
| Cooldown | Integer | 0 | 0..100 | Minimum number of ticks to wait between TickBase activations. |
| ForceGround | Toggle | false | — | When enabled, TickBase only considers tick snapshots where the player is on the ground, which can help ensure critical hits land. |
| Line | Color | — | — | Colour of the in-world line that visualises the simulated tick path. Set alpha to 0 to hide the line entirely. |
| RequiresKillAura | Toggle | true | — | When enabled, TickBase only activates if [KillAura](/docs/modules/combat/killaura) is running and its clicker is predicted to fire at the selected tick. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleTickBase.kt)*
