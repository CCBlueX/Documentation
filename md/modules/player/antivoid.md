## AntiVoid

AntiVoid keeps you from plunging into the void by looking a few ticks ahead and predicting whether your current fall will end with nothing solid beneath you. If it decides you're about to drop into nothingness, it steps in automatically and pulls you back to safety, then shows a notification so you know it acted.

This is handy on servers and maps with bottomless pits, bridge gaps, or void-edge arenas — for example when knockback, a missed jump, or a removed block sends you over the edge. It stays out of the way during normal play and only reacts when a genuine void fall is detected. It also holds off while you're flying with [Fly](/docs/modules/movement/fly) or bridging with [Scaffold](/docs/modules/world/scaffold), so it won't interfere with those.

The **Mode** setting decides how the rescue is performed: *GhostBlock* spawns an invisible block under you to catch the fall, *Flag* lifts you back upward, *Blink* holds your movement back (similar to [Blink](/docs/modules/player/blink)) so the dangerous fall is never committed to the server, and *UseItem* uses a configured hotbar or offhand item — useful on servers where a power-up item cancels void death.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Mode | Mode Selector | Blink | — | How AntiVoid rescues you: GhostBlock catches you on a fake block, Flag lifts you upward, Blink holds back your movement to avoid the fall, UseItem uses a configured item to cancel the fall. |
| Mode → Flag → FallDistance | Decimal | 1.05 | 0.0..6.0 | How far you must have fallen before the Flag rescue lifts you back up. |
| Mode → Flag → Height | Decimal | 0.42 | 0.01..10.0 | How high the Flag rescue nudges you upward to break the fall. |
| Mode → Flag → Silent | Toggle | false | — | When on, applies the upward correction through movement packets rather than visibly snapping your position. |
| Mode → UseItem → YMotionThreshold | Decimal | -0.5 | -1.0..-0.1 | How fast you must be falling before UseItem reacts; your downward y motion must drop below this value. |
| Mode → UseItem → SlotResetDelay | Integer Range | 4..6 | 0..40 | How long, in ticks, to keep the item selected after using it before switching back. |
| Mode → UseItem → Items | Registry List | Magma Cream | — | The items UseItem looks for in your hotbar and offhand; the closest matching slot is used. |
| VoidLevel | Integer | 0 | -256..0 | The height that counts as the start of the void; AntiVoid treats a fall toward this level with nothing below as a void fall. |

---
*Last updated: 2026-07-28 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/antivoid/ModuleAntiVoid.kt)*
