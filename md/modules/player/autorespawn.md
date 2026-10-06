## AutoRespawn

AutoRespawn takes the waiting out of dying. The moment the death screen appears, the module respawns you automatically and closes the screen, so you're back in the world without clicking the "Respawn" button yourself. It's handy on PvP and survival servers where dying often means a race back to your loot or your teammates — every saved fraction of a second counts.

Internally it watches for the game's [DeathScreen and immediately calls respawn](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoRespawn.kt#L38-L47). Note that the respawn button isn't actually clickable for the first 20 ticks (one second) after death; if you respawn faster than the server expects, use the **Delay** setting to hold off for a set number of ticks before triggering. With the default of 0, it fires as soon as the screen is detected.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Delay | Integer | 0 | 0..20 | How long to wait, in ticks, after the death screen appears before respawning. The respawn button only becomes clickable 20 ticks after death, so increase this if respawning instantly causes issues. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoRespawn.kt)*
