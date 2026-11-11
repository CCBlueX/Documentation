## BetterTab

BetterTab improves the player list you see while holding <kbd>Tab</kbd>. You can sort players, show more of them, color yourself and your friends, see exact ping numbers, and hide players you do not want to see.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Sorting | Choice | Vanilla | Vanilla, Ping, NameLength, DisplayNameLength, Alphabetical, ReverseAlphabetical, None | How players are ordered. Vanilla keeps the server's order. |
| Visibility | Multi-Select | Header, Footer | Header, Footer, NameOnly | Header and Footer show the server's text above and below the list. NameOnly shows only player names. |
| Limits → TabSize | Integer | 80 | 1..1000 | Most players shown in the list. |
| Limits → ColumnHeight | Integer | 20 | 1..100 | Rows in each column before a new column starts. |
| Highlight | Toggleable Group | On | | Colors the background of some players. |
| Highlight → Self | Toggleable Group | On | | Colors your own name. |
| Highlight → Self → Color | Color | Green | | Color for you. |
| Highlight → Friends | Toggleable Group | On | | Colors your friends. |
| Highlight → Friends → Color | Color | Blue | | Color for friends. |
| Highlight → Others | Toggleable Group | On | | Colors players that match the names below. |
| Highlight → Others → Color | Color | Gray | | Color for those players. |
| Highlight → Others → Filter → FilterBy | Multi-Select | DisplayName, PlayerName | DisplayName, PlayerName | Check the name shown in the list, the account name, or both. |
| Highlight → Others → Filter → Names | Editable List | | | Name patterns to color. |
| AccurateLatency | Toggleable Group | On | | Shows each player's ping as a number instead of bars. |
| AccurateLatency → AppendMSSuffix | Toggle | true | | Adds `ms` after the number. |
| PlayerHider | Toggleable Group | Off | | Hides players that match the names below. |
| PlayerHider → Filter → FilterBy | Multi-Select | DisplayName, PlayerName | DisplayName, PlayerName | Check the name shown in the list, the account name, or both. |
| PlayerHider → Filter → Names | Editable List | | | Name patterns to hide. |
| ShowGameMode | Toggle | true | | Shows each player's game mode. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleBetterTab.kt)*
