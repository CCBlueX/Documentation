## Freeze

Freeze locks you in place on your own screen without the server immediately reacting to it. Depending on the mode you pick, it either holds back your outgoing packets so they pile up (like a controlled lag spike), drops them entirely, or keeps you network-connected while only your movement is suspended. This is handy for dodging an incoming hit, lining up a play, or stalling while the server still believes everything is normal.

The **Queue** mode buffers your packets and releases them later, similar to [Blink](/docs/modules/player/blink), so your character snaps forward once they're flushed. **Cancel** simply discards packets in the chosen direction, meaning that movement is lost rather than delayed. **Stationary** is the stealthiest option: it freezes your position but keeps talking to the server, sending small rotation tweaks so anticheats don't flag the unusual behavior, which makes it the best choice on stricter servers.

Because freezing your packets can desync you from the server, you may get teleported back ("flagged") when the connection catches up. Use **DisableOnFlag** to automatically switch the module off when that happens, and turn on **BalanceWarp** if you want the held-up movement to be replayed smoothly when you disable Freeze instead of being thrown away.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Queue | Queue, Cancel, Stationary | Chooses how Freeze holds you in place: queuing packets for later, cancelling them, or staying connected while only stopping movement. |
| Mode → Queue → Origin | Multi-Select | Outgoing | Incoming, Outgoing | Which packet direction gets queued up and released later. |
| Mode → Cancel → Origin | Multi-Select | Outgoing | Incoming, Outgoing | Which packet direction gets discarded while frozen. |
| Mode → Stationary → CancelC0B | Toggle | true | — | Holds back ping-response packets to better slip past stricter anticheat timer checks while frozen. |
| DisableOnFlag | Toggle | false | — | Automatically turns Freeze off if the server teleports you back, helping you recover from a desync. |
| Notification | Toggle | false | — | Shows an on-screen notice when Freeze disables itself after being flagged. |
| BalanceWarp | Toggle | false | — | Replays the movement that was held back when you disable Freeze, instead of discarding it. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleFreeze.kt)*
