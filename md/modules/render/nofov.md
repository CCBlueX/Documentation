## NoFOV

NoFOV stops your field of view from changing. Normally the game zooms in and out when you sprint, draw a bow or get a speed or slowness effect.

**Constant** always uses one fixed field of view. **Custom** keeps some of the zooming but lets you make it weaker and set limits.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Constant | Constant, Custom | How your field of view is kept steady. |
| Mode → Constant → FOV | Integer | 90 | 1 to 179 | The field of view in degrees that is always used. |
| Mode → Custom → BaseFOV | Decimal | 1.0 | 0.0 to 1.5 | The base zoom level that is always added. |
| Mode → Custom → Limit | Decimal Range | 0.0 to 1.5 | 0.0 to 1.5 | The lowest and highest zoom level allowed. |
| Mode → Custom → Multiplier | Decimal | 1.0 | 0.1 to 1.5 | How much of the game's own zooming still comes through. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleNoFov.kt)*
