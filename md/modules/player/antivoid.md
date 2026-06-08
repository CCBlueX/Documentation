## AntiVoid

AntiVoid keeps you from plunging into the void by looking a few ticks ahead and predicting whether your current fall will end with nothing solid beneath you. If it decides you're about to drop into nothingness, it steps in automatically and pulls you back to safety, then shows a notification so you know it acted.

This is handy on servers and maps with bottomless pits, bridge gaps, or void-edge arenas — for example when knockback, a missed jump, or a removed block sends you over the edge. It stays out of the way during normal play and only reacts when a genuine void fall is detected. It also holds off while you're flying with [Fly](/docs/modules/movement/fly) or bridging with [Scaffold](/docs/modules/world/scaffold), so it won't interfere with those.

The **Mode** setting decides how the rescue is performed: *GhostBlock* spawns an invisible block under you to catch the fall, *Flag* lifts you back upward, and *Blink* holds your movement back (similar to [Blink](/docs/modules/player/blink)) so the dangerous fall is never committed to the server.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Mode | Mode Selector | Blink | — | How AntiVoid rescues you: GhostBlock catches you on a fake block, Flag lifts you upward, Blink holds back your movement to avoid the fall. |
| Mode → Flag → FallDistance | Decimal | 1.05 | 0.0..6.0 | How far you must have fallen before the Flag rescue lifts you back up. |
| Mode → Flag → Height | Decimal | 0.42 | 0.01..10.0 | How high the Flag rescue nudges you upward to break the fall. |
| Mode → Flag → Silent | Toggle | false | — | When on, applies the upward correction through movement packets rather than visibly snapping your position. |
| VoidLevel | Integer | 0 | -256..0 | The height that counts as the start of the void; AntiVoid treats a fall toward this level with nothing below as a void fall. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/antivoid/ModuleAntiVoid.kt)*
