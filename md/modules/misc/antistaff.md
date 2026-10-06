## AntiStaff

AntiStaff warns you when a server's staff members appear in your game. When you join a supported server, LiquidBounce fetches that server's known staff list and watches for those accounts. The moment a listed staff member shows up in the player list, you get an in-game chat warning and a notification — so you know to play it safe while someone may be keeping an eye on you.

This module relies on a community-maintained list of staff usernames tied to each server's domain. If a server has no list available, you'll simply get a notice that none was found, and no alerts will fire for that server.

Enable **ShowInTabList** to additionally highlight detected staff directly in the tab player list, making them easy to spot at a glance.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| ShowInTabList | Toggle | true | — | Highlights detected staff members directly in the tab player list so they're easy to spot. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAntiStaff.kt)*
