## ClientChat

Connects you to LiquidChat, a chat for LiquidBounce users. You can talk to other users even when you play on different servers. LiquidChat messages show up in your normal chat with the sender's player head in front.

**Aliases:** GlobalChat, IRC  
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Enabled | Toggle | On | | Connects to LiquidChat. Turn it off to leave the chat. |
| Filter | Toggleable Group | Off | | Hides messages from some users. |
| Filter → Usernames | Text List | (empty) | | The users the filter is about. Upper and lower case do not matter. |
| Filter → UsernameFilter | Choice | Blacklist | Whitelist, Blacklist | Blacklist hides messages from the users on the list. Whitelist only shows messages from the users on the list. |
| AutoTranslate | Multi-Select | (none) | PublicChat, PrivateChat | Translates messages from the chosen chats into your language. The [AutoTranslate](/docs/global-settings/auto-translate) settings choose the service, and `.autotranslate language set <code>` chooses the language. |
| AllowMessages | Toggle | On | | Lets other users send you private messages. Changing it reconnects you to LiquidChat. |

### Chatting

- `.chat <message>` writes to everyone in LiquidChat.
- `.liquidchat msg <user> <message>` (or `.lc msg`) sends a private message.
- `.liquidchat report <user> <reason>` reports a user who breaks the rules.

When you switch Minecraft accounts, or log in or out of your LiquidBounce account, the client reconnects to LiquidChat with the new account. If a message gets deleted from LiquidChat, it also disappears from your chat.

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/global/GlobalSettingsClientChat.kt)*
