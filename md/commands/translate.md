## Translation Commands

Translation commands allow you to translate text between languages using the configured translation provider.

---

### `.translate`

Translate text from one language to another.

**Aliases:** `tr`

**Usage:**
```
.translate <source> <target> <text>
```

**Parameters:**
- `source` (required) — The source language code (e.g. `en`, `de`, `ja`). Use `auto` for automatic detection.
- `target` (required) — The target language code.
- `text` (required, vararg) — The text to translate.

**Example:**
```
.translate en de Hello, how are you?
.translate auto en Hallo, wie geht es dir?
.tr ja en こんにちは
```

### Common Language Codes

| Code | Language |
|---|---|
| `auto` | Auto-detect |
| `en` | English |
| `de` | German |
| `fr` | French |
| `es` | Spanish |
| `ja` | Japanese |
| `ko` | Korean |
| `zh` | Chinese |
| `ru` | Russian |
| `pt` | Portuguese |
| `it` | Italian |

---

### `.autotranslate`

Configure the target language for the auto-translation feature.

**Subcommands:**
- `.autotranslate language set <code>` — Set the target language for auto-translation.

**Parameters:**
- `code` — A language code (e.g. `en`, `de`).

**Example:**
```
.autotranslate language set en
.autotranslate language set de
```

> **Tip:** Auto-translation works with the [ClientChat](/docs/Global%20Settings/ClientChat) global setting. Enable the AutoTranslate option in ClientChat to automatically translate incoming LiquidChat messages.
