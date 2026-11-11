## TextFieldProtect

TextFieldProtect shows stars (`*`) instead of what you type when it matches one of your patterns. By default it hides `/register`, `/login` and `/email` commands, so nobody watching your screen or stream sees your password. The server still gets the real text.

To hide your name too, use [NameProtect](/docs/modules/misc/nameprotect).

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Patterns | Editable List | ^/register.*, ^/login.*, ^/email.* | | Text to hide (as regex patterns). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleTextFieldProtect.kt)*
