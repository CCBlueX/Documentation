## TextFieldProtect

TextFieldProtect masks the visible content of chat input fields whenever what you type matches one of your configured patterns. Instead of showing the actual text on screen, the field displays asterisks (`*`) — keeping sensitive input hidden from anyone who might be watching your screen, recording your gameplay, or sharing your screen via stream or video.

By default, the module protects commands commonly used on auth-required servers: `/register`, `/login`, and `/email`. These are the commands most likely to contain passwords or personal information you wouldn't want exposed. You can customise the list by adding or removing regex patterns to cover any other commands or text you want masked.

This module only affects what is *rendered* on screen — the actual text you type is sent to the server normally. It is purely a visual privacy safeguard. Consider pairing it with [NameProtect](/docs/modules/misc/nameprotect) if you also want to hide your username from on-screen display.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Patterns | Editable List | — | — | A list of regex patterns. Any text field whose full content matches one of these patterns will have its rendered text replaced with asterisks. Defaults include `^/register.*`, `^/login.*`, and `^/email.*`. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleTextFieldProtect.kt)*
