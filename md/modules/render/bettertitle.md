## BetterTitle

Improvements to the on-screen title and subtitle. Its main feature is optionally running incoming titles and subtitles through the client's [Auto Translate](/docs/global-settings/auto-translate) so foreign-language announcements can be read in your own language.

**Category:** Render
**Aliases:** BetterSubtitle
**Enabled by default:** No

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── AutoTranslate (Toggleable Group | default: off)
    ├── Components (Multi-Select | options: Title, Subtitle)
    └── ShowIn (Multi-Select | default: Chat | options: Chat, Message)
```

### Settings Details

#### AutoTranslate

Toggleable group (default: off) that translates incoming title text using the global Auto Translate service.

- **Components** (Multi-Select) — options: `Title`, `Subtitle` — Which parts of the on-screen title to translate.
- **ShowIn** (Multi-Select) — default: `Chat`; options: `Chat`, `Message` — Where the translated text is displayed. `Chat` prints the translation as a chat line; `Message` replaces the on-screen title/subtitle text itself.

> Auto Translate must be configured for translation to work — see [Auto Translate](/docs/global-settings/auto-translate).

### Screenshots

*Screenshots for BetterTitle will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleBetterTitle.kt)*
