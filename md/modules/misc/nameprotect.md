## NameProtect

NameProtect replaces player usernames with custom text everywhere they appear on your client — in chat, above heads, in the tab list, and anywhere else names are rendered. Your own username is always replaced with whatever you set in **Replacement**. This makes it ideal for recording videos or streaming without accidentally revealing your Minecraft account name.

Beyond protecting your own name, NameProtect can also obscure the names of your friends list and any other online players. Friends are replaced using their alias (if set) or a generated default name, while other players receive a randomised but deterministic pseudonym. In all cases the replacement is purely client-side — other players on the server see nothing different.

Each category of name replacement (yours, friends, others) can be coloured independently using either a static colour or a cycling rainbow effect, making it easy to distinguish at a glance which names have been substituted and who belongs to which group.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Replacement | Text | — | — | The text your own username is replaced with everywhere it appears client-side. |
| ColorMode | Mode Selector | Static | Static, Rainbow | Colour applied to your own replaced username. |
| ColorMode → [Static] → Color | Color | — | — | Static colour used for your own replaced username when ColorMode is set to Static. |
| ObfuscateOthers | Toggleable Group | off | — | When enabled, replaces the names of all other online players (who are not friends) with random pseudonyms. |
| ObfuscateOthers → ColorMode | Mode Selector | Static | Static, Rainbow | Colour applied to other players' replaced names. |
| ObfuscateOthers → ColorMode → [Static] → Color | Color | — | — | Static colour used for other players' replaced names when their ColorMode is set to Static. |
| ObfuscateFriends | Toggleable Group | on | — | When enabled, replaces the names of players on your friends list with their alias or a generated name. |
| ObfuscateFriends → ColorMode | Mode Selector | Static | Static, Rainbow | Colour applied to friends' replaced names. |
| ObfuscateFriends → ColorMode → [Static] → Color | Color | — | — | Static colour used for friends' replaced names when their ColorMode is set to Static. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/nameprotect/ModuleNameProtect.kt)*
