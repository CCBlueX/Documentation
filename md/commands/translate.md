## Translation Commands

These commands translate text into another language. The translation service is picked in the [AutoTranslate](/docs/global-settings/auto-translate) settings.

---

### `.translate`

Translates text from one language into another. Short form: `.tr`.

```
.translate <from> <to> <text>
```

- `from`: the language of the text. Use `auto` to let the service guess it.
- `to`: the language you want.
- `text`: the text to translate. It can have spaces.

```
.translate en de Hello, how are you?
.translate auto en Hallo, wie geht es dir?
.tr ja en こんにちは
```

Languages are written as short codes. Press Tab to see all of them. Some common ones:

| Code | Language |
|---|---|
| `en` | English |
| `de` | German |
| `fr` | French |
| `es` | Spanish |
| `it` | Italian |
| `pt` | Portuguese |
| `ru` | Russian |
| `ja` | Japanese |
| `ko` | Korean |
| `zh` | Chinese |

---

### `.autotranslate`

Sets the language that chat messages are translated into when automatic translation is on. It starts as `en` and is the same as the LanguageCode setting in [AutoTranslate](/docs/global-settings/auto-translate). Automatic translation is used by [Client Chat](/docs/global-settings/client-chat) and the BetterChat and BetterTitle modules.

- `.autotranslate language`: shows the current language.
- `.autotranslate language set <code>`: sets the language.

```
.autotranslate language set de
```

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/command/commands/translate)*
