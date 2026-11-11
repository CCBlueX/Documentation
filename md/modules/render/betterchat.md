## BetterChat

BetterChat makes the chat nicer to use. It can keep old messages, stop servers from clearing your chat, hide spam, translate messages and add text to everything you send.

With Copy on, hold Shift and left-click a chat line to copy it. Right-click a line to put its text into your chat box.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Features | Multi-Select | Infinite, AntiClear, KeepAfterDeath | Infinite, AntiClear, KeepAfterDeath, ForceUnicodeChat | Infinite removes the chat length limit. AntiClear stops servers from clearing your chat. KeepAfterDeath lets you chat on the death screen. ForceUnicodeChat turns your letters into wide Unicode letters. |
| AutoTranslate | Multi-Select | | ChatMessage, DisguisedChatMessage, GameMessage | Which kinds of messages get translated. The translation shows up in chat. |
| AppendPrefix | Toggleable Group | Off | | Adds text to the start of every message you send. |
| AppendPrefix → Prefix | Text | `> ` | | The text added at the start. |
| AppendSuffix | Toggleable Group | Off | | Adds text to the end of every message you send. |
| AppendSuffix → Suffix | Text | ` \| 𝙻𝚒𝚚𝚞𝚒𝚍𝙱𝚘𝚞𝚗𝚌𝚎` | | The text added at the end. |
| AntiSpam | Toggleable Group | On | | Cuts down on spam in chat. |
| AntiSpam → StackMessages | Toggle | false | | Shows a repeated message once with a `[count]` instead of many times. |
| AntiSpam → Filters | Editable List | | | Patterns of messages to hide. |
| Copy | Toggleable Group | On | | Lets you copy chat lines by clicking them. |
| Copy → Notify | Toggle | true | | Shows a notification when a line is copied. |
| Copy → Highlight | Toggle | true | | Highlights the line under your mouse. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/betterchat/ModuleBetterChat.kt)*
