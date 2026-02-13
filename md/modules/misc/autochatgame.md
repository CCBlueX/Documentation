## AutoChatGame

Uses OpenAI to play chat games.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── BaseUrl (Text)
├── OpenAiKey (Text)
├── Model (Text)
├── ReactionTime (Integer Range | default: 1000..5000 | range: 0..10000 | ms)
├── Cooldown (Integer | default: 2 | range: 0..60 | minutes)
├── BufferTime (Integer | default: 200 | range: 0..500 | ms)
├── TriggerSentence (Text)
├── IncludeTrigger (Toggle | default: true)
├── ServerName (Text)
├── AnswerTemplate (Text)
└── Prompt (Text)
```

### Settings Details

- **BaseUrl** (Text)
- **OpenAiKey** (Text)
- **Model** (Text)
- **ReactionTime** (Integer Range) — default: `1000` – `5000`; range: `0` – `10000`; unit: ms
- **Cooldown** (Integer) — default: `2`; range: `0` – `60`; unit: minutes
- **BufferTime** (Integer) — default: `200`; range: `0` – `500`; unit: ms
- **TriggerSentence** (Text)
- **IncludeTrigger** (Toggle) — default: `true`
- **ServerName** (Text)
- **AnswerTemplate** (Text)
- **Prompt** (Text)

### Screenshots

*Screenshots for AutoChatGame will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleAutoChatGame.kt)*
