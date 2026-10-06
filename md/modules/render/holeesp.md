## HoleESP

HoleESP highlights nearby "holes" — safe one-block spots you can stand in during crystal PvP so that incoming end crystal explosions deal little or no damage. As you move around, it scans the surrounding terrain and renders a colored marker on every qualifying gap, color-coded by the type of hole so you can tell at a glance which spots are the safest. Bedrock-bottomed 1x1 holes get their own color since they can't be mined out from below.

It's a render-only helper that pairs naturally with offensive crystal tools like [CrystalAura](/docs/modules/combat/crystalaura) and defensive setups like [Surround](/docs/modules/world/surround) — letting you spot where to retreat or where an opponent is likely to hide. You can choose between a solid box outline or a glowing floor plane, tune how far it scans horizontally and vertically, and have distant holes fade out so the view stays clean.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | GlowingPlane | Box, GlowingPlane | How holes are drawn: a full outlined box, or a glowing plane rising from the floor. |
| Mode → Box → Outline | Toggle | true | — | Draws a border around each box for clearer edges. |
| Mode → GlowingPlane → Outline | Toggle | true | — | Outlines the floor of each glowing plane for clearer edges. |
| Mode → GlowingPlane → GlowHeight | Decimal | 0.7 | 0.0..1.0 | How tall the glowing gradient rises from the floor of the hole. |
| HorizontalScanDistance | Integer | 32 | 4..128 | Maximum horizontal distance (in blocks) at which holes are detected and shown. |
| VerticalScanDistance | Integer | 8 | 4..128 | Maximum vertical distance (in blocks) at which holes are detected and shown. |
| DistanceFade | Decimal | 0.3 | 0.0..1.0 | How strongly markers fade out as they get farther away; 0 disables fading. |
| 1x1Bedrock | Color | — | — | Color used for 1x1 holes with a bedrock floor. |
| 1x1 | Color | — | — | Color used for standard 1x1 holes. |
| 1x2 | Color | — | — | Color used for 1x2 holes. |
| 2x2 | Color | — | — | Color used for 2x2 holes. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleHoleESP.kt)*
