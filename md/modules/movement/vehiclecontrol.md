## VehicleControl

VehicleControl lets you fly with any ride: boats, horses, minecarts, striders, pigs and more. Hold jump to go up, sneak to go down and the walk keys to move. When you press neither jump nor sneak, Glide makes the ride slowly sink (or rise, if you set it above 0).

Hold sprint to use the faster SprintSpeed values. MouseControl turns the ride to where you look. While the module is on you can only get off when the ride is on the ground or in water, so you do not fall by accident.

Rehook gets you off the ride and back on again every few ticks (20 per second), which helps on some anti-cheats. For a speed boost when you get off a ride, see [VehicleBoost](/docs/modules/movement/vehicleboost).

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| BaseSpeed → Horizontal | Decimal | 0.5 | 0.1..10.0 | Speed forward and sideways. |
| BaseSpeed → Vertical | Decimal | 0.35 | 0.1..10.0 | Speed up and down. |
| SprintSpeed | Toggleable Group | on | | Uses the speeds below while you hold sprint. |
| SprintSpeed → Horizontal | Decimal | 5.0 | 0.1..10.0 | Speed forward and sideways while sprinting. |
| SprintSpeed → Vertical | Decimal | 2.0 | 0.1..10.0 | Speed up and down while sprinting. |
| Glide | Decimal | -0.15 | -0.3..0.3 | Up and down speed when you press neither jump nor sneak. Below 0 sinks, above 0 rises. |
| MouseControl | Toggle | false | | Turns the ride to where you look. |
| NoGlideOnSprint | Toggle | false | | Turns off Glide while you sprint, so you stay at the same height. |
| Rehook | Toggleable Group | off | | Gets off and back on the ride over and over. |
| Rehook → UnhookAfter | Integer | 4 | 1..10 | Ticks on the ride before getting off. |
| Rehook → HookAfter | Integer | 2 | 1..10 | Ticks off the ride before getting back on. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleVehicleControl.kt)*
