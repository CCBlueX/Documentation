## AutoTranslate

Configures the translation provider used for automatic message translation throughout the client, including LiquidChat auto-translation and the `.translate` command.

### Settings

```
└── Provider (Mode Selector | default: GoogleTranslate | modes: GoogleTranslate)
```

### Settings Details

- **Provider** (Mode Selector) — default: `GoogleTranslate`; modes: `GoogleTranslate` — Selects the translation service used for all translation features. Currently only Google Translate is available.

### Related Features

- **ClientChat AutoTranslate** — When enabled in [ClientChat](/docs/Global%20Settings/ClientChat), incoming LiquidChat messages are automatically translated using this provider.
- **`.translate` command** — Uses this provider to translate text between languages on demand.
- **`.autotranslate` command** — Configures the target language for auto-translation.
