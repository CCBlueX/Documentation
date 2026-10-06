## NoSlotSet

NoSlotSet prevents servers from forcibly changing your selected hotbar slot. Normally, a server can send a packet that switches your held item to a specific slot — a technique used by some minigame servers or anti-cheat systems to control what you are holding. With NoSlotSet enabled, those forced slot-change packets are blocked and your current slot selection is preserved.

This module pairs naturally with tools that manage your hotbar silently, such as [SilentHotbar](/docs/modules/render/silenthotbar), since it ensures neither the server nor incoming packets can override what slot the client is actually reporting. It is most useful on servers that interfere with hotbar control as part of their game mechanics or anti-cheat behaviour.

**Category:** Player
**Enabled by default:** No

### Settings

This module has no configurable settings.

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleNoSlotSet.kt)*
