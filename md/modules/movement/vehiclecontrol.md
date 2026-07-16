## VehicleControl

VehicleControl gives you full aerial and speed control while riding any vehicle — boats, horses, minecarts, striders, pigs, and more. Once enabled, your movement keys drive the vehicle in every direction: hold Jump to rise, hold Sneak to descend, and walk keys to travel horizontally. A configurable Glide value produces a slight passive descent when you are not actively pressing any vertical key, preventing the vehicle from shooting upward uncontrollably. Positive Glide values make the vehicle gently rise on its own instead.

Two speed tiers let you tune travel pace precisely. BaseSpeed applies at all times; when you hold the sprint key the module switches to the (much faster) SprintSpeed values instead, giving you a quick boost for open-air travel. Enabling MouseControl makes the vehicle yaw track your look direction, so you can steer with your mouse exactly like walking on foot. If you prefer the vehicle to stay perfectly level during sprints, toggle NoGlideOnSprint to suppress the passive vertical drift whenever sprint speeds are active.

The Rehook sub-group is an anti-cheat bypass. When enabled it rhythmically dismounts you from the vehicle for a brief window and then immediately remounts, cycling on a tick-based schedule controlled by UnhookAfter and HookAfter. This disrupts the continuous riding signature that some anti-cheat plugins use to flag vehicle flight. While VehicleControl is active, dismounting mid-air is blocked — you can only sneak off a vehicle when it is on the ground or in water, so accidental drops are avoided. See also [VehicleBoost](/docs/modules/movement/vehicleboost) for a complementary approach to vehicle speed. While [SpearKill](/docs/modules/combat/spearkill) performs a spear dash, its dash velocity takes over the vehicle's movement, so the attack also works while riding.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Glide | Decimal | -0.15 | -0.3 – 0.3 | Passive vertical velocity applied when the vehicle is not in water and no vertical key is pressed. Negative values cause a slow descent; positive values cause a slow ascent. |
| MouseControl | Toggle | false | — | Rotates the vehicle to match your look direction each tick, enabling full mouse-steered flight. |
| NoGlideOnSprint | Toggle | false | — | Suppresses the Glide effect while the sprint key is held, keeping the vehicle at a constant altitude during sprint-speed movement. |
| BaseSpeed → Horizontal | Decimal | 0.5 | 0.1 – 10.0 | Horizontal movement speed applied when not sprinting. |
| BaseSpeed → Vertical | Decimal | 0.35 | 0.1 – 10.0 | Vertical movement speed (Jump / Sneak) applied when not sprinting. |
| SprintSpeed | Toggleable Group | on | — | When enabled, replaces BaseSpeed values with the speeds below while the sprint key is held. |
| SprintSpeed → Horizontal | Decimal | 5.0 | 0.1 – 10.0 | Horizontal movement speed while sprinting. |
| SprintSpeed → Vertical | Decimal | 2.0 | 0.1 – 10.0 | Vertical movement speed while sprinting. |
| Rehook | Toggleable Group | off | — | Periodically dismounts and re-mounts the vehicle on a fixed tick schedule to help evade anti-cheat detection of sustained vehicle flight. |
| Rehook → UnhookAfter | Integer | 4 | 1 – 10 | Number of ticks to remain mounted before the module dismounts you during each rehook cycle. |
| Rehook → HookAfter | Integer | 2 | 1 – 10 | Number of ticks to wait after dismounting before re-mounting during each rehook cycle. |

---
*Last updated: 2026-07-16 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/master/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleVehicleControl.kt)*
