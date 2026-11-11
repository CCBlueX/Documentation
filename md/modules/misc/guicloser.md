## GUICloser

Some servers open menus you didn't ask for, like vote or shop windows. GUICloser closes a menu right away when its title matches one of your filters.

Not sure what a menu is called? Turn on PrintScreenTitle. The title of every menu you open then shows up in chat, and you can click it to copy it.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Matches | Matches, Contains | Matches closes a menu only if the whole title fits a filter. Contains closes it if a filter appears anywhere in the title. |
| Filter | Editable List | ^Vote$ | | Titles to close (as regex patterns). |
| PrintScreenTitle | Toggle | false | | Writes the title of each menu you open into chat. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleGUICloser.kt)*
