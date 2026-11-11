## NoWeb

NoWeb stops cobwebs from slowing you down. Normally a cobweb makes you almost stop.

The default Air mode lets you walk through webs like they are not there. The other modes are for servers with an anti-cheat. Grim-2.3.65 breaks each web you touch. Intave-14.8.4 is made for Intave servers. PlaceWater puts water next to the web to wash it away and then picks the water back up, so you need a water bucket in your hotbar or offhand. Strafe pushes you along while you are inside a web.

NoWeb turns off [AvoidHazards](/docs/modules/movement/avoidhazards) when AvoidHazards is in Shape mode with cobwebs selected, because that mode makes webs solid. AvoidHazards in Input mode only walks around webs and works fine together with NoWeb.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Air | Air, Grim-2.3.65, Intave-14.8.4, PlaceWater, Strafe | How NoWeb gets you through webs. |
| Mode → [Grim-2.3.65] → BreakOnWorld | Toggle | true | | Also removes the web on your screen when it is broken. |
| Mode → [PlaceWater] → Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [PlaceWater] → Pickup | Toggleable Group | on | | Picks the water back up after it washed the web away. |
| Mode → [PlaceWater] → Pickup → PickupSpan | Decimal Range | 0.8..3.0 | 0.5..20.0 s | How many seconds after placing the water it tries to pick it up. |
| Mode → [Strafe] → Strength | Decimal | 0.23 | 0.01..0.8 | How hard you are pushed forward inside a web. |
| Mode → [Strafe] → MotionY | Toggleable Group | off | | Sets your up and down speed inside a web. |
| Mode → [Strafe] → MotionY → MotionYStrength | Decimal | 0.6 | -2.0..2.0 | Up and down speed inside a web. Positive moves you up, negative moves you down. |
| Mode → [Strafe] → OnlyOnGround | Toggle | false | | Only pushes you while you stand on the ground. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/noweb/ModuleNoWeb.kt)*
