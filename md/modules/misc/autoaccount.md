## AutoAccount

Many cracked (offline-mode) servers require you to log in or register with a password before you can play, usually by typing a command like `/login <password>` or `/register <password> <password>`. AutoAccount watches incoming server messages and does this for you automatically, so you don't have to retype your password every time you join.

When the server prompts you, the module fills in your stored password and sends the matching login or register command after a short, randomized delay so it looks more natural. It detects prompts by matching configurable patterns against the text it sees, and it can read those prompts from the chat, the on-screen title, and the subtitle. Tell it which password to use, set the command names and detection patterns to suit your server, and pick which message sources it should listen to.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Password | Text | — | — | The password sent when logging in or registering. |
| Delay | Integer Range | 21..23 | 0..50 ticks | Randomized wait before sending the command, picked between the low and high values to vary timing. |
| RegisterCommand | Text | — | — | The command name used to register an account (the password is appended automatically). |
| LoginCommand | Text | — | — | The command name used to log in (the password is appended automatically). |
| RegisterRegex | Text | — | — | Pattern matched against server messages to detect a registration prompt. |
| LoginRegex | Text | — | — | Pattern matched against server messages to detect a login prompt. |
| RepeatPasswordOnRegister | Toggle | true | — | Whether the register command sends the password twice (`/register <password> <password>`) or only once (`/register <password>`). |
| MessageSource | Multi-Select | [Chat, Title, Subtitle] | [Chat, Title, Subtitle] | Which sources to scan for login/register prompts. |

---
*Last updated: 2026-07-19 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoAccount.kt)*
