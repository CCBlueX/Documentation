## AutoTranslate

Chooses the service that translates text for LiquidBounce. It is used by the [`.translate`](/docs/commands/translate) command, by [Client Chat](/docs/global-settings/client-chat) when it translates LiquidChat messages, and by the BetterChat and BetterTitle modules. Set the language to translate into with the LanguageCode setting or `.autotranslate language set <code>`.

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| LanguageCode | Text | `en` | | The language that text is translated into, as a short code such as `de`. See [Translation Commands](/docs/commands/translate) for common codes. |
| Provider | Mode Selector | Google | Google, LibreTranslate | The translation service. Google works without any setup. LibreTranslate uses a LibreTranslate server of your choice. |
| Provider → [LibreTranslate] → BaseUrl | Text | `https://libretranslate.com` | | Address of the LibreTranslate server. |
| Provider → [LibreTranslate] → ApiKey | Text | (empty) | | Your key for that server. Leave it empty if the server does not need one. |

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/global/GlobalSettingsAutoTranslate.kt)*
