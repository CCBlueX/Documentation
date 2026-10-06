## AutoLeave

AutoLeave watches your health and pulls you off the server the moment things get dangerous. As soon as your health drops to or below the configured threshold, the module disconnects you automatically — handy on combat servers where a clutch escape is better than a death and the loot loss that comes with it.

You can fine-tune how aggressively it reacts with the **Delay** setting, and choose *how* you leave with **Mode**: a clean quit, or one of several deliberately malformed actions that force the server to kick you. AutoLeave ignores the threshold in singleplayer, in creative mode, and while you're holding a Totem of Undying, since in those cases you're not at real risk of dying.

Once it triggers and you leave, the module disables itself so it won't keep firing.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Health | Decimal | 8.0 | 0.0..20.0 HP | The health threshold that triggers leaving. When your health reaches or falls below this value, AutoLeave activates. |
| Delay | Integer Range | 0..0 | 0..60 ticks | How long your health must stay at or below the threshold before you actually leave, in ticks. A random value is picked from this range each time, and the timer resets if your health recovers. |
| Mode | Choice | Quit | Quit, InvalidPacket, SelfHurt, IllegalChat, IllegalSwitchitem, IllegalInteract | How you disconnect. *Quit* leaves the server normally, while the other modes deliberately trigger a server-side kick (via an invalid packet, self-damage, illegal chat, an illegal item switch, or an illegal interaction) so it looks like a connection issue rather than a manual leave. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoLeave.kt)*
