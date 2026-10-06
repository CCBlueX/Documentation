## MurderMystery

MurderMystery is a helper module designed for use on servers running the Murder Mystery mini-game (such as Hypixel). It automatically identifies and highlights dangerous players — murderers and those with bows — so you always know who to watch out for or run from. Detected murderers are highlighted in red, while detectives and players carrying bows are highlighted in blue, making threats immediately visible at a glance.

The module supports three game-mode variants to match whichever Murder Mystery variant you are playing. **Classic** mode watches for players who pick up a sword (or sword-like item) and announces the murderer in chat with an audio cue. **Infection** mode tracks the first infected player and monitors bow holders, helping you avoid zombie-like threats as the round progresses. **Assassination** mode reads your in-game contract map to identify your assassination target and listens for audio cues to detect the player assigned to hunt you down — both are then flagged as threats. In all modes, a highlighted box is drawn around any dropped bow lying on the ground so you can easily spot it. When **SetTeamPrefix** is enabled, the module also prepends a short tag (`[MURD]` or `[BOW]`) to flagged players' names in the tab list and above their heads, making roles clear at all times.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| SetTeamPrefix | Toggle | true | — | When enabled, adds a `[MURD]` or `[BOW]` prefix to detected players' names in the tab list and nametags. |
| Mode | Mode Selector | Classic | Classic, Infection, Assassination | Selects which Murder Mystery variant the module operates in. Classic tracks sword-holders as murderers; Infection tracks the first infected player and survivors with bows; Assassination reads your contract map and sound cues to identify your target and assassin. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/murdermystery/ModuleMurderMystery.kt)*
