## AutoDisable

AutoDisable watches for specific in-game events and automatically turns off the modules you've chosen, so you don't get caught with cheats still running at the wrong moment. For example, you can have it switch everything off the instant an anticheat flags you, the moment you die, or right before you disconnect — situations where leaving a module active could give you away or cause problems.

Use the **Modules** list to pick which modules AutoDisable should switch off. By default it's set up to manage [Fly](/docs/modules/movement/fly), [Speed](/docs/modules/movement/speed), [NoClip](/docs/modules/movement/noclip), and [KillAura](/docs/modules/combat/killaura), but you can add or remove any module you like. The **On** setting controls which events trigger the shutdown. Whenever a trigger fires and at least one of your selected modules was active, you'll get a notification telling you why they were disabled.

This pairs well with legit-style play: combine it with the "Flag" trigger to bail out automatically the first time a server's anticheat reacts to you.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Modules | Registry List | — | — | The list of modules that get disabled when a trigger fires. |
| On | Multi-Select | [Flag, Death, WorldChange] | [Flag, Death, WorldChange, Disconnect] | Which events trigger the shutdown: being flagged by an anticheat, dying, changing worlds, or disconnecting. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleAutoDisable.kt)*
