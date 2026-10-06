## BetterTab

BetterTab reworks Minecraft's player list (the overlay shown while holding <kbd>Tab</kbd>) with several quality-of-life upgrades. Instead of the vanilla list that's capped at 80 entries and sorted by the server, you can re-sort players, highlight important people, expand how many names fit on screen, and clean up clutter you don't want to see.

Use it on busy servers where the tab list is crowded or hard to read: bump the row/column limits so everyone fits, sort by ping to spot laggers, or [sort alphabetically and by name length](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleBetterTab.kt#L116-L130) to find people quickly. The Highlight group tints the background behind yourself, your friends, and any custom-matched players so they're easy to pick out, while AccurateLatency replaces the vanilla 5-bar ping icon with the real millisecond value. PlayerHider goes a step further and removes matching players from the list entirely.

Highlighting and hiding both use a [name filter](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleBetterTab.kt#L92-L114) that matches against the in-game display name and/or the raw account name using your list of patterns, so you control exactly who is affected.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Sorting | Choice | Vanilla | Vanilla, Ping, NameLength, DisplayNameLength, Alphabetical, ReverseAlphabetical, None | How players are ordered in the tab list. `Vanilla` keeps the server's order, `Ping` sorts by latency, `NameLength`/`DisplayNameLength` by name length, `Alphabetical`/`ReverseAlphabetical` by account name, and `None` leaves entries unsorted. |
| Visibility | Multi-Select | [Header, Footer] | Header, Footer, NameOnly | Chooses which parts of the tab list are shown. `Header` and `Footer` display the server's banner text above/below the list; `NameOnly` strips entries down to just the player name. |
| ShowGameMode | Toggle | true | — | Shows each player's game mode in the tab list. |
| Limits → TabSize | Integer | 80 | 1..1000 | Maximum number of players shown in the tab list (vanilla caps at 80). |
| Limits → ColumnHeight | Integer | 20 | 1..100 | Maximum number of rows per column before the list wraps into a new column. |
| Highlight | Toggleable Group | on | — | Tints the background behind chosen players to make them stand out. |
| Highlight → Self | Toggleable Group | on | — | Highlights your own entry in the list. |
| Highlight → Self → Color | Color | — | — | Background color used for your own entry. |
| Highlight → Friends | Toggleable Group | on | — | Highlights players on your friends list. |
| Highlight → Friends → Color | Color | — | — | Background color used for friends. |
| Highlight → Others | Toggleable Group | on | — | Highlights any other players that match the filter below. |
| Highlight → Others → Color | Color | — | — | Background color used for matched players. |
| Highlight → Others → Filter → FilterBy | Multi-Select | [DisplayName, PlayerName] | DisplayName, PlayerName | Which name to match against: the in-game `DisplayName`, the raw account `PlayerName`, or both. |
| Highlight → Others → Filter → Names | Editable List | — | — | Regex patterns of names to highlight; an entry matches if any pattern matches the selected name(s). |
| AccurateLatency | Toggleable Group | on | — | Replaces the vanilla ping-bar icon with each player's exact latency value. |
| AccurateLatency → AppendMSSuffix | Toggle | true | — | Appends the `ms` unit suffix after the latency number. |
| PlayerHider | Toggleable Group | off | — | Removes players matching the filter from the tab list entirely. |
| PlayerHider → Filter → FilterBy | Multi-Select | [DisplayName, PlayerName] | DisplayName, PlayerName | Which name to match against: the in-game `DisplayName`, the raw account `PlayerName`, or both. |
| PlayerHider → Filter → Names | Editable List | — | — | Regex patterns of names to hide; an entry is hidden if any pattern matches the selected name(s). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleBetterTab.kt)*
