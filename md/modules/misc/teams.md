## Teams

Teams works alongside [KillAura](/docs/modules/combat/killaura) and other combat modules to prevent them from attacking players who are recognized as your teammates. When enabled, it intercepts targeting decisions and suppresses attacks on anyone it identifies as being on your side, letting you fight safely in team-based gamemodes without friendly-fire accidents.

Teammate detection is flexible and can combine several independent methods. **ScoreboardTeam** relies on Minecraft's native scoreboard team system, which is used on many servers that assign players to formal teams. **NameColor** treats two players as teammates if their display names share the same text color — a common convention on servers that color-code teams. **Prefix** compares the first word of each player's display name and considers players teammates when it matches, which works well on servers like Hypixel BedWars or GommeHD Skywars that prepend a team tag. You can also enable **ArmorColor** slot checks: if you select one or more armor slots, any player whose dye color on those pieces matches yours will be treated as a teammate.

Beyond protecting teammates from attacks, Teams also colours their entity highlights based on your chosen **ColorSources** — using their scoreboard team colour, their armor dye colour, or both — so teammates stand out clearly in modules like [ESP](/docs/modules/render/esp).

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Matches | Multi-Select | ScoreboardTeam, NameColor | — | Detection methods used to identify teammates. `ScoreboardTeam` uses Minecraft's scoreboard team system. `NameColor` treats players with the same name text color as teammates. `Prefix` compares the first word of display names (useful on servers like Hypixel BedWars or GommeHD Skywars). |
| ArmorColor | Multi-Select | *(none)* | — | Armor slots to compare dye colors for teammate detection. When one or more slots are selected, a player whose armor color in those slots matches yours is treated as a teammate. Options: `Feet`, `Legs`, `Chest`, `Head`. |
| ColorSources | Multi-Select | Team, Armor | — | Color sources used to tint teammate entity highlights. `Team` applies the scoreboard team color; `Armor` uses the dye color of the configured armor slots. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleTeams.kt)*
