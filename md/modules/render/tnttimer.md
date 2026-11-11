## TNTTimer

TNTTimer shows which TNT is lit and how long until it explodes. Lit TNT blinks red, and blinks faster the closer it is to exploding. With **ShowTimer** on, a countdown sits on each TNT and turns from yellow to red. When the TNT is off screen, an arrow at the screen edge points to it.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ESP | Toggle | true | | Makes lit TNT glow and blink red. |
| ShowTimer | Toggleable Group | off | | Shows a countdown on each lit TNT. |
| ShowTimer → Scale | Curve | | Distance 0 to 200, Scale 0.25 to 4 | Size of the countdown at each distance. |
| ShowTimer → RenderY | Decimal | 1.0 | -2.0 to 2.0 | Moves the countdown up or down. |
| ShowTimer → OwnerName | Toggle | true | | Adds the name of the player who lit the TNT. |
| ShowTimer → TimeUnit | Choice | Ticks | Ticks, Seconds | Shows the time in ticks (20 per second) or in seconds. |
| ShowTimer → Show | Multi-Select | InView, Offscreen | InView, Offscreen | **InView** shows countdowns on TNT you can see. **Offscreen** shows them with an arrow at the screen edge for TNT you can't see. At least one must stay on. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleTNTTimer.kt)*
