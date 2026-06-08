## ReportHelper

ReportHelper automates the process of reporting players on servers that support report commands or confirmation GUIs. When enabled, it can detect when another player's name appears alongside your own in chat — a common pattern on servers like Hypixel when you are killed or interacted with — and automatically issue a report command for that player, saving you the effort of typing it manually every time.

The module is split into two independently toggleable sub-features. **AutoReport** watches incoming chat messages for your name and another online player's name appearing together, then fires your configured report command at that player after a short delay. It keeps track of already-reported players per session so no one is reported twice. **AutoConfirm** handles the confirmation step: when a report confirmation GUI appears (such as the yes/no terracotta screen on Hypixel or the diamond-sword selection screen on Heypixel), it automatically clicks the confirm option and closes the screen for you.

Note that neither friends (managed via LiquidBounce's friend list) nor yourself will ever be auto-reported. Both sub-features are off by default and must be toggled on individually to take effect.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| AutoReport | Toggleable Group | off | — | Automatically sends a report command when another player's name appears with yours in chat. |
| AutoReport → Delay | Integer Range | 1..3 | 0..20 ticks | How many ticks to wait before sending the report command after a trigger is detected. |
| AutoReport → Chance | Integer | 100 | 1..100 % | Percentage chance that a detected player will actually be reported. Set below 100 to report only some of the time. |
| AutoReport → CommandPattern | Text | — | — | The command template used to report a player. Use `%s` as a placeholder for the player's name (e.g. `report %s`). |
| AutoConfirm | Toggleable Group | off | — | Automatically confirms report GUIs when they appear. |
| AutoConfirm → Mode | Mode Selector | Hypixel | — | Which server's confirmation GUI layout to handle. `Hypixel` clicks the green terracotta yes-button in a 9×3 inventory; `Heypixel` selects the diamond sword in a 9×1 inventory. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/reporthelper/ModuleReportHelper.kt)*
