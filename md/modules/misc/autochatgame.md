## AutoChatGame

Some servers run small games in chat, like "first to type this word" or quick math questions. AutoChatGame asks an AI for the answer and types it into chat for you.

You need your own API key from OpenAI or Anthropic. Put it in ApiKey, or the module turns itself off. Other AI services that work like OpenAI (for example DeepSeek, OpenRouter, Groq or Ollama) also work if you set BaseUrl. Answers take a moment, and how good they are depends on the model.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Protocol | Choice | OpenAiCompatible | OpenAiCompatible, Anthropic | Which kind of AI service you use. |
| BaseUrl | Text | | | Address of the AI service. Leave it empty to use the normal OpenAI or Anthropic address. |
| ApiKey | Text | | | Your API key. Required. |
| Model | Text | gpt-4o-mini | | Which AI model answers. |
| ReactionTime | Integer Range | 1000..5000 | 0..10000 ms | Random wait before the answer is sent, so it looks like a person typed it. |
| Cooldown | Integer | 2 | 0..60 minutes | Wait after answering before it answers again. |
| BufferTime | Integer | 200 | 0..500 ms | How long it keeps reading chat after the trigger to get the whole question. |
| TriggerSentence | Text | Chat Game | | Text in chat that starts a new game. |
| IncludeTrigger | Toggle | true | | Also gives the line with the trigger to the AI. |
| ServerName | Text | Minecraft | | Server name the AI is told about. |
| AnswerTemplate | Text | %s | | How the answer is written. `%s` is the answer. Start it with `/` to send a command. |
| Prompt | Text | | | Instructions for the AI. Best left as it is. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoChatGame.kt)*
