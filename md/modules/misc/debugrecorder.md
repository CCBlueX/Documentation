## DebugRecorder

DebugRecorder is a tester's tool that captures raw gameplay data and saves it to disk for later analysis. As the seed description says, it's mainly of interest to developers and people helping the LiquidBounce team gather training data — it doesn't give you any in-game advantage by itself. When you enable it, it starts recording; when you disable it, it writes everything it collected to a timestamped `.json` file inside the `debug-recorder` folder and shows a clickable link in chat so you can open it. If nothing was captured, it simply tells you no packets were recorded.

What gets recorded depends on the selected **Mode**. The combat-focused modes (Combat, CombatTrainer) log how you aim and move relative to nearby targets, which is used to build samples for the client's aiming systems. CPS logs your click and swing timing, Aim logs rotation and target data each tick, Box logs hitbox vectors for the entity under your crosshair, and Generic logs general entity debug info on demand. CombatTrainer even spawns practice slimes around you and records your attempts to hit them.

Because it's a diagnostic utility, DebugRecorder turns itself off automatically when you leave a server and is excluded from saved configs, so it won't accidentally stay on. Unless you've been asked to gather data, you can safely leave it alone.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Mode | Mode Selector | Generic | Combat, CombatTrainer, Generic, CPS, Aim, Box | Selects which kind of data is captured while the module is enabled. |
| Mode → [Combat] → Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/debugrecorder/ModuleDebugRecorder.kt)*
