## Debug

Debug shows what other modules are working out behind the scenes, like where they aim, which target they picked and which path they expect you to take. It draws lines and boxes in the world and shows a list of values on your screen. It gives you no advantage in a game. Use it when you test a module like [KillAura](/docs/modules/combat/killaura) or [Scaffold](/docs/modules/world/scaffold), or when you report a bug.

The values show up as one small table per module and fade out after a few seconds. Hold the player list key (Tab) to hide them. If the tables do not fit on screen, open the chat and scroll with the mouse wheel.

Many modules report at once, so **TitleFilter** lets you only show the ones whose name matches a pattern. With **DebugLog** on, the values are also saved to a file in the `debug-log` folder of your LiquidBounce folder, which you can attach to a bug report.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Parameters | Toggle | true | | Shows the list of values that modules report. |
| Global | Toggle | false | | Also shows values from parts of the client that are not modules, such as the timer, combat and inventory handling. |
| Geometry | Toggle | true | | Draws the lines, boxes and points that modules report into the world. |
| Expires | Integer | 5 | 1 to 30 secs | How long a value stays on screen. |
| Width | Integer | 180 | 120 to 400 px | How wide each table is. |
| TitleFilter | Text | `.*` | | Only shows modules whose name matches this pattern. `.*` matches all of them. |
| DebugLog | Toggle | false | | Also saves the values to a file in the `debug-log` folder. A new file starts each time you turn the module on. |
| SimulatedPlayer | Toggleable Group | Off | | Draws a line showing where you will move next. |
| SimulatedPlayer → TicksToPredict | Integer | 20 | 5 to 100 | How far ahead the line goes, in ticks (20 per second). |
| Graph | Toggleable Group | Off | | Shows a small graph of the curve below on your screen. |
| Graph → Curve | Curve | | | The curve shown in the graph. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/debug/ModuleDebug.kt)*
