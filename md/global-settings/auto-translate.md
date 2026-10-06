## AutoTranslate

Configures the translation provider used for automatic message translation throughout the client, including LiquidChat auto-translation and the `.translate` command.

Successful translations are cached, so translating the same text between the same two languages again returns the stored result instead of contacting the provider. The cache holds up to 512 translations, each entry is discarded 15 minutes after it was stored, and switching the provider clears it completely.

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
