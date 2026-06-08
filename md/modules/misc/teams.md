## Teams

Prevents KillAura from attacking team mates.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Matches (Multi-Select | default: [ScoreboardTeam, NameColor] | options: ScoreboardTeam, NameColor, Prefix)
├── ArmorColor (Multi-Select | default: [Head] | options: Feet, Legs, Chest, Head)
└── ColorSources (Multi-Select | default: [Team, Armor] | options: Team, Armor)
```

### Settings Details

- **Matches** (Multi-Select) — default: `ScoreboardTeam`, `NameColor`; options: `ScoreboardTeam`, `NameColor`, `Prefix`
- **ArmorColor** (Multi-Select) — default: `Head`; options: `Feet`, `Legs`, `Chest`, `Head`
- **ColorSources** (Multi-Select) — default: `Team`, `Armor`; options: `Team`, `Armor` — Which sources to take the teammate highlight color from: the scoreboard team color and/or dyed armor color. Can be set to none to disable coloring.

### Screenshots

*Screenshots for Teams will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleTeams.kt)*
