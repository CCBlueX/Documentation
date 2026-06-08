## NoClip

NoClip lets you move freely through solid blocks as if they weren't there. Once enabled, your character ignores all collision with the terrain, letting you glide through walls, floors, ceilings, and other solid geometry. To activate it reliably, let a falling block (such as sand or gravel) land on your head first — this nudges the server into a state where the movement is accepted.

While inside blocks you control your movement direction with your normal walk keys, rise with Jump, and descend with Sneak. If you are riding a vehicle, NoClip applies to the vehicle as well (unless [VehicleControl](/docs/modules/movement/vehiclecontrol) is also running, in which case that module handles the vehicle's movement instead).

Keep in mind that anti-cheat systems can issue a setback (a forced position correction from the server) when they detect unusual movement. When **DisableOnSetback** is on, NoClip will turn itself off the moment a setback is received and warn you in chat, helping you avoid getting stuck in a loop of corrections.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Speed | Decimal | 0.23 | 0.1 – 0.4 | How fast you move in any direction while noclipping. |
| OnlyInVehicle | Toggle | false | — | When enabled, NoClip only takes effect while you are riding a vehicle; it pauses automatically when you are on foot. |
| DisableOnSetback | Toggle | false | — | Automatically disables the module and prints a warning if the server sends a position correction (setback), indicating the anti-cheat has flagged the movement. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleNoClip.kt)*
