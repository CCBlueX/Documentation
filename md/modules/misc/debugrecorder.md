## DebugRecorder

DebugRecorder is a tool for the LiquidBounce developers. It records how you play and saves it to a file, and it gives you nothing in the game. Unless the team asked you to record something, leave it off.

Turn it on to start recording. When you turn it off, it saves a file in the `debug-recorder` folder and puts a link to it in chat. The mode picks what gets recorded. CombatTrainer spawns practice slimes around you to hit. The module turns off when you leave a server.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Generic | Combat, CombatTrainer, Generic, CPS, Aim, Box | What to record. |
| Mode → [Combat] → Target | Setting Group | | | See [Shared: Target](/docs/modules/shared-settings/target). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/debugrecorder/ModuleDebugRecorder.kt)*
