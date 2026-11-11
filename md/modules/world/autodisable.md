## AutoDisable

AutoDisable turns off the modules you pick when something happens, like when the anticheat catches you or when you die. You get a message telling you why.

By default it turns off [Fly](/docs/modules/movement/fly), [Speed](/docs/modules/movement/speed), [NoClip](/docs/modules/movement/noclip) and [KillAura](/docs/modules/combat/killaura). You can add or remove modules in the list.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Modules | Registry List | Fly, Speed, NoClip, KillAura | | Modules to turn off. |
| On | Multi-Select | Flag, Death, WorldChange, Disconnect | Flag, Death, WorldChange, Disconnect | When to turn them off: when the anticheat pulls you back, when you die, when you change worlds or when you leave the server. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleAutoDisable.kt)*
