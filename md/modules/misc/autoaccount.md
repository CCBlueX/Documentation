## AutoAccount

Many cracked servers make you type `/login <password>` or `/register <password> <password>` every time you join. AutoAccount types it for you after a short wait. It looks for the server's request in chat and in the big title text on screen.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Password | Text | a1b2c3d4 | | The password it sends. Change it to your own. |
| Delay | Integer Range | 3..5 | 0..50 ticks | How long to wait before sending, in ticks (20 per second). |
| RegisterCommand | Text | register | | The command used to register. |
| LoginCommand | Text | login | | The command used to log in. |
| RegisterRegex | Text | /register | | Text that shows the server wants you to register. |
| LoginRegex | Text | /login | | Text that shows the server wants you to log in. |
| RepeatPasswordOnRegister | Toggle | true | | Sends the password twice when registering. |
| MessageSource | Multi-Select | Chat, Title, Subtitle | Chat, Title, Subtitle | Where to look for the server's request. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoAccount.kt)*
