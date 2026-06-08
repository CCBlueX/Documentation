## AutoChatGame

AutoChatGame automatically plays the chat-based mini-games that many servers run in their global chat — things like first-to-type, math problems, true/false questions, and word unscrambles. It watches the server's chat for a trigger phrase, gathers the question that follows, sends it to OpenAI for an answer, and then types that answer back into chat for you.

To use it you must provide your own OpenAI API key in **OpenAiKey** — the module will disable itself and warn you if the key is blank. You can also point it at a different API endpoint or model if you prefer. Because it relies on an external AI service, answers are not instant, and the quality depends on the model you choose.

To stay believable, AutoChatGame waits a randomized **ReactionTime** before sending each answer and enforces a **Cooldown** so it won't answer the same round twice. You can tailor it to a specific server by setting the **TriggerSentence** that marks the start of a game, the **ServerName** the AI is told about, and an **AnswerTemplate** for how the reply is formatted (including sending it as a command). The **Prompt** is pre-tuned for chat games and is best left unchanged.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| BaseUrl | Text | — | — | The OpenAI-compatible API endpoint to send requests to. Change this only if you use a custom or proxy server. |
| OpenAiKey | Text | — | — | Your OpenAI API key. Required — the module disables itself if this is empty. |
| Model | Text | — | — | The AI model used to generate answers. |
| ReactionTime | Integer Range | 1000..5000 ms | 0..10000 ms | A random delay within this range before the answer is sent, to make responses look more human. |
| Cooldown | Integer | 2 minutes | 0..60 | Minimum wait between answering rounds, preventing the same game from being answered twice. |
| BufferTime | Integer | 200 ms | 0..500 | How long after the trigger phrase to keep collecting chat lines as part of the question. |
| TriggerSentence | Text | — | — | The phrase in chat that signals a new chat-game question has started. |
| IncludeTrigger | Toggle | true | — | Whether the line containing the trigger phrase is included as part of the question. |
| ServerName | Text | — | — | The server name given to the AI for context, helping it answer server-specific questions. |
| AnswerTemplate | Text | — | — | How the answer is formatted before sending. If the result starts with "/", it is sent as a command. |
| Prompt | Text | — | — | The instructions given to the AI. Pre-optimized for chat games; changing it is not recommended. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoChatGame.kt)*
