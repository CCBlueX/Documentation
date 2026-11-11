## ReportHelper

ReportHelper reports players for you. AutoReport watches the chat: when a message has your name and another player's name in it, like a kill message, it sends a report command for that player. AutoConfirm clicks the confirm button in the report menu that some servers open afterwards.

Each player is only reported once until you leave the server. Your friends are never reported. Both parts are off at first, so turn on the ones you want.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| AutoReport | Toggleable Group | Off | | Reports a player when their name shows up in chat together with yours. |
| AutoReport → Delay | Integer Range | 1..3 | 0..20 ticks | Ticks (20 per second) to wait before sending the report. |
| AutoReport → Chance | Integer | 100 | 1..100 % | How likely it is that a player gets reported. |
| AutoReport → CommandPattern | Text | `report %s` | | The report command. `%s` is replaced with the player's name. |
| AutoConfirm | Toggleable Group | Off | | Confirms the report menu when it opens. |
| AutoConfirm → Mode | Mode Selector | Hypixel | Hypixel, Heypixel | Which server's report menu to click. Hypixel clicks the green yes button, Heypixel clicks the diamond sword. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/reporthelper/ModuleReportHelper.kt)*
