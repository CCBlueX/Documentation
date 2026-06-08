## InventoryMove

InventoryMove lets you walk, jump, and sneak while any inventory or container screen is open. Normally, Minecraft blocks all movement input when a GUI is active; this module forwards your keypresses through to the movement system so you can reposition, dodge threats, or keep strafing without closing the screen first.

The **Behavior** setting controls how cautiously the module operates. **Normal** passes all movement through regardless of what screen is open. **Safe** closes the inventory server-side the moment you start moving, so the server never sees you moving inside a handled screen — clicks are also blocked while you are in motion. **Undetectable** stops your movement input entirely when a container screen (chests, crafting tables, etc.) is open, effectively disabling the module for those screens while still working in your personal inventory. **StopOnAction** takes a different approach: it queues any inventory interaction packets and only sends them once you have stopped moving, keeping your movement and inventory actions mutually exclusive.

By default, the Sneak key is not forwarded through open screens (it tends to conflict with GUI behaviour); enable **PassthroughSneak** if you want sneak input to also be passed while an inventory is open. The optional **SprintControl**, **SneakControl**, **Timer**, and **Blink** sub-groups give you fine-grained control over sprint/sneak state and can add a tick-speed boost or a [Blink](/docs/modules/player/blink)-style packet delay while you navigate screens.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Behavior | Choice | Normal | Normal, Safe, Undetectable, StopOnAction | Controls how movement input is handled while a screen is open. Normal passes all input through. Safe closes the inventory server-side when movement begins and blocks clicks during motion. Undetectable suppresses movement inside container screens. StopOnAction queues inventory interaction packets until you stop moving. |
| PassthroughSneak | Toggle | false | — | When enabled, the Sneak key is also forwarded as movement input while a screen is open. |
| SprintControl | Toggleable Group | off | — | When enabled, overrides the sprint state on the client and/or server side while a screen is open. |
| SprintControl → Client | Choice | DoNotChange | DoNotChange, ForceSprint, ForceNoSprint | Controls the client-side sprint state while an inventory screen is open. |
| SprintControl → Server | Choice | DoNotChange | DoNotChange, ForceSprint, ForceNoSprint | Controls the server-side sprint state reported while an inventory screen is open. |
| SneakControl | Toggleable Group | off | — | When enabled, overrides the sneak state on the client side while a screen is open. |
| SneakControl → Client | Choice | DoNotChange | DoNotChange, ForceSneak, ForceNoSneak | Forces or suppresses the sneak state on the client while an inventory screen is open. |
| Timer | Toggleable Group | off | — | When enabled, adjusts the game timer speed while an inventory screen is open. |
| Timer → Speed | Decimal | 1.0 | 0.1 – 2.0 | Multiplier applied to the game timer while a screen is open. Values above 1.0 speed up the tick rate; values below 1.0 slow it down. |
| Blink | Toggleable Group | off | — | When enabled, holds outgoing movement packets while a screen is open and flushes them when the screen closes, similar to [Blink](/docs/modules/player/blink). |
| Blink → MaximumTime | Integer | 10000 | 0 – 30000 ms | Maximum time in milliseconds to hold packets before automatically closing the screen and flushing the queued movement. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/inventorymove/ModuleInventoryMove.kt)*
