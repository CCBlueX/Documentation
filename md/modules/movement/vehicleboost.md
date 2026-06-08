## VehicleBoost

VehicleBoost launches you forward (and upward) the moment you dismount any vehicle — whether that's a boat, minecart, horse, pig, or any other rideable entity. Instead of simply dropping off and landing where the vehicle stopped, you get a configurable burst of momentum the instant you leave your ride.

This is useful for quickly closing distance on an enemy after chasing them in a vehicle, escaping a tight spot by bailing from a boat or minecart and immediately rocketing away, or chaining vehicle travel with fast ground movement. The boost fires once per dismount, using your facing direction to determine which way you fly horizontally.

You can tune the strength of both the horizontal thrust and the upward pop separately. A higher **HorizontalSpeed** flings you further forward, while **VerticalSpeed** controls how high you arc — useful if you need to clear terrain or just want a flat burst without much air time.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| HorizontalSpeed | Decimal | 2.0 | 0.1 – 10.0 | How fast you are launched horizontally in your facing direction when leaving a vehicle. |
| VerticalSpeed | Decimal | 1.0 | 0.1 – 5.0 | How strongly you are launched upward when leaving a vehicle. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleVehicleBoost.kt)*
