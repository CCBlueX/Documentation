## NoClip

NoClip lets you fly through walls, floors and ceilings. Use your walk keys to move, Jump to go up and Sneak to go down. When you ride something, it goes through blocks with you, unless [VehicleControl](/docs/modules/movement/vehiclecontrol) is on and steers it instead.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Speed | Decimal | 0.32 | 0.1..0.4 | How fast you move. |
| OnlyInVehicle | Toggle | false |  | Only works while you ride something. |
| DisableOnSetback | Toggle | true |  | Turns NoClip off and warns you in chat when the server pulls you back. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleNoClip.kt)*
