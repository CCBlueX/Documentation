## AutoAccount

Automatically authenticates you on cracked servers.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Password (Text)
├── Delay (Integer Range | default: 3..5 | range: 0..50 | ticks)
├── RegisterCommand (Text)
├── LoginCommand (Text)
├── RegisterRegex (Text)
├── LoginRegex (Text)
└── MessageSource (Multi-Select | default: [Chat, Title, Subtitle] | options: Chat, Title, Subtitle)
```

### Settings Details

- **Password** (Text)
- **Delay** (Integer Range) — default: `3` – `5`; range: `0` – `50`; unit: ticks
- **RegisterCommand** (Text)
- **LoginCommand** (Text)
- **RegisterRegex** (Text)
- **LoginRegex** (Text)
- **MessageSource** (Multi-Select) — default: `Chat`, `Title`, `Subtitle`; options: `Chat`, `Title`, `Subtitle`

### Screenshots

*Screenshots for AutoAccount will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleAutoAccount.kt)*
