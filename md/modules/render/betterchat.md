## BetterChat

Improvements to the in-game chat.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Features (Multi-Select | default: [Infinite, AntiClear, KeepAfterDeath] | options: Infinite, AntiClear, KeepAfterDeath, ForceUnicodeChat)
├── AutoTranslate (Multi-Select | options: ChatMessage, DisguisedChatMessage, GameMessage)
├── AppendPrefix (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   └── Prefix (Text)
├── AppendSuffix (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   └── Suffix (Text)
└── AntiSpam (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── StackMessages (Toggle | default: false)
    └── Filters (Editable List)
```

### Settings Details

- **Features** (Multi-Select) — default: `Infinite`, `AntiClear`, `KeepAfterDeath`; options: `Infinite`, `AntiClear`, `KeepAfterDeath`, `ForceUnicodeChat` — Selects which chat enhancement features to enable.
- **AutoTranslate** (Multi-Select) — options: `ChatMessage`, `DisguisedChatMessage`, `GameMessage` — Automatically translates incoming messages of the selected chat types.
#### AppendPrefix

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Enables prepending a prefix to outgoing messages.
- **Prefix** (Text) — The text to prepend to outgoing chat messages.

#### AppendSuffix

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Enables appending a suffix to outgoing messages.
- **Suffix** (Text) — The text to append to outgoing chat messages.

#### AntiSpam

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables anti-spam chat filtering.
- **StackMessages** (Toggle) — default: `false` — Combines duplicate messages into one with a counter.
- **Filters** (Editable List) — Regex patterns to filter out matching chat messages.


### Screenshots

*Screenshots for BetterChat will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2Fbetterchat%2FModuleBetterChat.kt)*
