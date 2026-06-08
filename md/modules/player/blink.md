## Blink

Blink holds your packets instead of sending them, making your character freeze in place on the server while you keep moving freely on your own screen. The moment the held packets are released, all your movement is replayed at once, so to everyone else it looks like you suddenly teleported across the world to wherever you've actually walked. By default it only delays your [outgoing](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleBlink.kt#L55) packets, but it can also suspend incoming ones.

Use it to escape a bad fight, set up an ambush, or buy time — while Blink is active the server still thinks you're standing where you started, so you take no real-world position updates. The held packets are flushed when you disable the module (or via AutoReset), at which point your true position is synced and the "teleport" happens. The actual queueing is handled by the [BlinkManager via the packet events](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleBlink.kt#L169-L174).

A few extras help with specific situations: **Dummy** spawns a clone of you at your starting spot so you can see where the server still thinks you are; **Ambush** auto-disables Blink the instant you attack or interact with an entity (releasing all packets so your hit lands from your real position); and if **AutoDodge** is also running, Blink will intelligently flush just enough packets to dodge incoming arrows. There's also a [tick-based AutoReset](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleBlink.kt#L148-L167) so the queue never builds up indefinitely.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Directions | Multi-Select | [Outgoing] | [Incoming, Outgoing] | Which packet directions to suspend. Outgoing holds the packets you send to the server (freezing your position server-side); Incoming holds packets coming from the server. At least one must be selected. |
| Dummy | Toggle | false | — | Spawns a visible clone of your character at your starting position, marking where the server still thinks you are while you move away. |
| Ambush | Toggle | false | — | Automatically disables Blink (releasing all held packets) the moment you attack, interact with, or spectate an entity, so the action lands from your real position. |
| AutoDisable | Toggle | true | — | When AutoReset triggers, also turns Blink off afterward instead of leaving it running. |
| AutoReset | Toggleable Group | off | — | When on, periodically clears or flushes the packet queue after a set number of ticks so it doesn't grow forever. |
| AutoReset → ResetAfter | Integer | 100 | 1..1000 | Number of movement ticks to wait before AutoReset fires. |
| AutoReset → ResetAction | Choice | Reset | [Reset, Blink] | What AutoReset does: Reset cancels and discards the queued packets; Blink flushes them (performing the teleport) and re-syncs the dummy clone. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleBlink.kt)*
