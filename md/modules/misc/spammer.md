## Spammer

Spammer automatically sends chat messages at timed intervals while the module is active. It is commonly used to repeatedly broadcast a message to other players — for advertising, reminders, or any other repetitive chat activity. Messages can be sourced either from a list you configure directly in the client settings, or from a plain-text file on your computer where each line is treated as a separate message.

Each cycle, Spammer picks a number of messages to send (within the **MPS** range), sends them, then waits a random amount of time (within the **Delay** range) before the next cycle. Any message beginning with `/` is sent as a server command instead of chat. Messages are capped at 256 characters; anything longer will be skipped with a warning.

Before sending, each message is modified to help evade simple chat filters. When **CustomFormatter** is disabled, a short random alphabetic prefix is prepended and the text is mixed-case; when it is enabled, you can embed placeholders directly in your messages — `%f` inserts a random decimal number, `%i` a random integer, `%s` a random short word, and `@a` is replaced with a random online player's name. The **MessageConverter** setting then applies an additional layer of text obfuscation on top of that.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Delay | Decimal Range | 2.0..4.0 | 0.0..300.0 secs | Time to wait between sending cycles. A random duration is chosen from within this range each time. |
| MPS | Integer Range | 1..1 | 1..500 messages | Number of messages to send per cycle. A random count within this range is used each cycle. |
| MessageSource | Mode Selector | Setting | — | Selects where messages are pulled from: a list entered in the settings (**Setting**) or a plain-text file on disk (**File**). |
| MessageSource → [Mode: Setting] → Message | Editable List | — | — | The list of messages to send. Add, remove, or reorder entries as needed. |
| MessageSource → [Mode: File] → Source | File | — | — | Path to a plain-text file where each line is treated as a separate message. |
| Pattern | Choice | Random | — | Order in which messages are selected. **Random** picks one at random each time; **Linear** cycles through them in sequence. |
| MessageConverter | Choice | Leet | — | Additional text transformation applied before sending. **None** sends the message as-is; **Leet** substitutes certain letters with numbers (e→3, a→4, etc.); **Random Case** randomly capitalises each character; **Random Space** randomly inserts extra spaces between characters. |
| CustomFormatter | Toggle | false | — | When enabled, messages support dynamic placeholders (`%f`, `%i`, `%s`, `@a`) for varied content each send. When disabled, a random short prefix is automatically prepended and random case is applied to the raw text. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleSpammer.kt)*
