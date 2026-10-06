## BetterTitle

Improvements to the on-screen title and subtitle. Its main feature is optionally running incoming titles and subtitles through the client's [Auto Translate](/docs/global-settings/auto-translate) so foreign-language announcements can be read in your own language.

**Category:** Render
**Aliases:** BetterSubtitle
**Enabled by default:** No

### Settings

Nested settings are shown with their group path, e.g. `Group → Setting`.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| AutoTranslate | Toggleable Group | off | — |  |
| AutoTranslate → Components | Multi-Select | [] | Title, Subtitle | Which parts of the on-screen title to translate. |
| AutoTranslate → ShowIn | Multi-Select | Chat | Chat, Message | Where the translated text is displayed. `Chat` prints the translation as a chat line; `Message` replaces the on-screen title/subtitle text itself. |

### Screenshots

*Screenshots for BetterTitle will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleBetterTitle.kt)*
