## GUICloser

GUICloser automatically closes container screens (chests, shops, voting menus, and other GUIs that a server forces open) the moment their title matches a word or phrase you've configured. This is handy on servers that pop up unwanted menus — vote reminders, shop prompts, or join GUIs — that interrupt what you're doing. When an unwanted screen opens and its title matches your filter, GUICloser instantly cancels it so you stay in the game.

To set it up, add the titles you want blocked to the **Filter** list and pick how strictly they should be matched with **Mode**. If you're not sure what a server actually names its screens, turn on **PrintScreenTitle** so the exact title of every container screen you open is printed to chat (and is click-to-copy), making it easy to build accurate filter entries.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Matches | Matches, Contains | How a screen title is compared against your filter entries. **Matches** closes a screen only when the whole title matches an entry, while **Contains** closes it when an entry appears anywhere in the title. |
| Filter | Editable List | — | — | The list of titles (entered as patterns) that GUICloser watches for. Any container screen whose title matches an entry, according to the selected Mode, is closed automatically. |
| PrintScreenTitle | Toggle | false | — | When enabled, prints the exact title of every container screen you open to chat as click-to-copy text, so you can build accurate filter entries. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleGUICloser.kt)*
