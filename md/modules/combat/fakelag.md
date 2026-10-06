## FakeLag

FakeLag makes your client briefly hold back the movement and action packets it would normally send to the server. Because the server only sees where you *were* a fraction of a second ago, enemies aiming at your real position will swing at empty space, and many attacks miss. The withheld packets are released ("flushed") shortly after, so to the server you simply appear to have a slightly laggy connection.

In **Dynamic** mode, FakeLag only holds packets back when an enemy is actually close and when lagging would genuinely move your visible position away from them — it stops lagging once your real position is closer to the threat than the held-back one, so you don't trap yourself in a bad spot. **Constant** mode lags all the time regardless of nearby enemies. Either way, packets are released immediately on important events such as taking damage, getting knocked back, being hit by an explosion, or receiving a position correction from the server, so you stay in sync when it matters.

Use **Range** and **Delay** to tune how aggressive the effect is, and **FlushOn** to decide which of your own actions (attacking, interacting with blocks, mining) should instantly end a lag and push your packets through. FakeLag also cooperates with [AutoDodge](/docs/modules/combat/autododge) to dodge arrows and with [AutoShoot](/docs/modules/combat/autoshoot) for bow play; for general packet-delaying outside of combat, see [Blink](/docs/modules/player/blink).

**Category:** Combat
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal Range | 3.0..3.5 | 0.0..10.0 | Distance (in blocks) at which an enemy is considered close enough to trigger lagging. |
| Delay | Integer Range | 300..300 | 0..1000 (ms) | How long packets are held back before being flushed; a random value is picked from this range each cycle. |
| RecoilTime | Integer | 0 | 0..1000 (ms) | Cooldown after a flush before FakeLag is allowed to start holding packets again. |
| Mode | Choice | Dynamic | Constant, Dynamic | Constant lags continuously; Dynamic only lags when an enemy is near and lagging actually moves you away from them. |
| FlushOn | Multi-Select | [EntityInteract, BlockInteract, Action] | EntityInteract, BlockInteract, Action | Which of your own actions instantly flush held packets: attacking/interacting with entities, interacting with blocks, or block actions like mining. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleFakeLag.kt)*
