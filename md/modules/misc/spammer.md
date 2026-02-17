## Spammer

Spams the chat with specified messages.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Delay (Decimal Range | default: 2.0..4.0 | range: 0.0..300.0 | secs)
├── MPS (Integer Range | default: 1..1 | range: 1..500 | messages)
├── MessageSource (Mode Selector | default: Setting | modes: Setting, File)
│   ├── [Mode: Setting]
│   │   └── Message (Editable List)
│   └── [Mode: File]
│       └── Source (File)
├── Pattern (Choice | default: RANDOM | options: Random, Linear)
├── MessageConverter (Choice | default: LEET_CONVERTER | options: None, Leet, Random Case, Random Space)
└── CustomFormatter (Toggle | default: false)
```

### Settings Details

- **Delay** (Decimal Range) — default: `2.0` – `4.0`; range: `0.0` – `300.0`; unit: secs
- **MPS** (Integer Range) — default: `1` – `1`; range: `1` – `500`; unit: messages
#### MessageSource

Select a mode for this feature. Available modes: **Setting**, **File**. Default: **Setting**.

##### Mode: Setting

- **Message** (Editable List)

##### Mode: File

- **Source** (File)

- **Pattern** (Choice) — default: `RANDOM`; options: `Random`, `Linear`
- **MessageConverter** (Choice) — default: `LEET_CONVERTER`; options: `None`, `Leet`, `Random Case`, `Random Space`
- **CustomFormatter** (Toggle) — default: `false`

### Screenshots

*Screenshots for Spammer will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleSpammer.kt)*
