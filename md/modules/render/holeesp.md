## HoleESP

HoleESP marks safe holes near you for crystal PvP. Standing in one of these holes protects you from most end crystal damage. Each kind of hole gets its own color, and 1x1 holes with a bedrock floor get a special one because they cannot be mined from below.

It works well with [CrystalAura](/docs/modules/combat/crystalaura) and [Surround](/docs/modules/world/surround).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | GlowingPlane | Box, GlowingPlane | Draw each hole as a box, or as a glow rising from the floor. |
| Mode → Box → Outline | Toggle | true | | Draws an outline around each box. |
| Mode → GlowingPlane → Outline | Toggle | true | | Draws an outline around the floor of each hole. |
| Mode → GlowingPlane → GlowHeight | Decimal | 0.7 | 0.0 to 1.0 | How high the glow goes. |
| HorizontalScanDistance | Integer | 32 | 4 to 128 | How far to the sides holes are found, in blocks. |
| VerticalScanDistance | Integer | 8 | 4 to 128 | How far up and down holes are found, in blocks. |
| DistanceFade | Decimal | 0.3 | 0.0 to 1.0 | How much far away holes fade out. 0 means no fading. |
| 1x1Bedrock | Color | #19C15C | | Color of 1x1 holes with a bedrock floor. |
| 1x1 | Color | #F7381B | | Color of 1x1 holes. |
| 1x2 | Color | #35BACC | | Color of 1x2 holes. |
| 2x2 | Color | #F7CF1B | | Color of 2x2 holes. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleHoleESP.kt)*
