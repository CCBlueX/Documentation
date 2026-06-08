## BetterChat

BetterChat bundles several quality-of-life improvements for Minecraft's in-game chat into a single Render module. Turn it on and pick which conveniences you want — there's no aiming or combat involved, just a nicer chat experience. Because the features are independent, you can run only the ones you care about (for example, keeping unlimited scrollback while ignoring the prefix/suffix tools).

The **Features** multi-select holds the core toggles: remove the usual line/length limits (`Infinite`), stop servers from wiping your chat history (`AntiClear`), let you open and type in chat from the death screen (`KeepAfterDeath`), and convert outgoing letters to full-width Unicode (`ForceUnicodeChat`). The AppendPrefix/AppendSuffix groups automatically wrap every message you send, AutoTranslate runs incoming messages through the client's translator, and AntiSpam either filters or stacks repeated lines. Copy lets you Shift+Left-click a chat line to copy it to your clipboard or Right-click it to drop the text into your chat box.

Under the hood, outgoing text passes through [`modifyMessage`](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/betterchat/ModuleBetterChat.kt#L170-L182), which applies the Unicode transform and then the prefix and suffix in order. AntiSpam's [stacking logic](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/betterchat/AntiSpam.kt#L59-L84) re-sends a duplicate message with a `[count]` suffix instead of spamming new lines, and tags message IDs as `external` so servers can't fake client-style messages.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Features | Multi-Select | [Infinite, AntiClear, KeepAfterDeath] | Infinite, AntiClear, KeepAfterDeath, ForceUnicodeChat | Core chat toggles. `Infinite` removes chat length/history limits, `AntiClear` blocks servers from clearing your chat, `KeepAfterDeath` lets you use chat on the death screen, and `ForceUnicodeChat` converts your outgoing letters to full-width Unicode characters. |
| AutoTranslate | Multi-Select | [] | ChatMessage, DisguisedChatMessage, GameMessage | Automatically translates the selected types of incoming messages using the client's translator and prints the result back into chat. |
| AppendPrefix | Toggleable Group | Off | — | When enabled, automatically adds your configured prefix to the start of every message you send. |
| AppendPrefix → Prefix | Text | `> ` | — | The text inserted before each outgoing message. |
| AppendSuffix | Toggleable Group | Off | — | When enabled, automatically adds your configured suffix to the end of every message you send. |
| AppendSuffix → Suffix | Text | ` \| 𝙻𝚒𝚚𝚞𝚒𝚍𝙱𝚘𝚞𝚗𝚌𝚎` | — | The text appended after each outgoing message. |
| AntiSpam | Toggleable Group | On | — | Reduces chat spam by filtering and/or stacking incoming messages. |
| AntiSpam → StackMessages | Toggle | false | — | Instead of printing duplicate messages repeatedly, replaces the existing line with a single one that shows a `[count]` of how many times it was received. Does not apply to disguised chat messages. |
| AntiSpam → Filters | Editable List | — | — | A list of regex patterns; any incoming message whose content matches a pattern is hidden from chat. |
| Copy | Toggleable Group | On | — | Enables copying chat lines: Shift+Left-click copies a line to your clipboard, Right-click inserts its text into the chat box. |
| Copy → Notify | Toggle | true | — | Shows a notification confirming when a chat line has been copied to your clipboard. |
| Copy → Highlight | Toggle | true | — | Highlights the chat line under your cursor so you can see which one will be copied. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/betterchat/ModuleBetterChat.kt)*
