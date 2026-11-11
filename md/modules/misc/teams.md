## Teams

Teams stops [KillAura](/docs/modules/combat/killaura) and other combat modules from hitting your teammates. It can find teammates by the server's teams, by name color, by the tag in front of the name, or by armor color. It also colors teammates in modules like [ESP](/docs/modules/render/esp) with their team or armor color.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Matches | Multi-Select | ScoreboardTeam, NameColor | ScoreboardTeam, NameColor, Prefix | How to find teammates. ScoreboardTeam uses the server's teams. NameColor checks if names have the same color. Prefix checks if the first word of the name is the same (for example on Hypixel BedWars). |
| ArmorColor | Multi-Select | Head | Feet, Legs, Chest, Head | Players whose dyed armor in these slots has the same color as yours are teammates. |
| ColorSources | Multi-Select | Team, Armor | Team, Armor | Which color to show teammates in. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleTeams.kt)*
