## AntiCheatDetect

AntiCheatDetect tries to figure out which anti-cheat is running on the server you're connected to and tells you about it in chat. Many servers use well-known anti-cheats (for example to catch movement or combat hacks), and knowing which one you're up against helps you decide how cautiously to play and which other modules are safe to use.

When you enable the module — and again once it has gathered enough information from the server — it prints the detected anti-cheat's name to your chat. If it can't identify the anti-cheat, it simply stays quiet. This module only detects and notifies; it does not bypass or interfere with anything, so pair it with modules like [AntiStaff](/docs/modules/misc/antistaff) or [FlagCheck](/docs/modules/misc/flagcheck) if you want more protective behavior.

**Category:** Misc
**Enabled by default:** No

### Settings

This module has no configurable settings.

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAntiCheatDetect.kt)*
