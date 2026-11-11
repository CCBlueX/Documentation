## Derp

Derp makes your head spin, twitch and look in random directions for other players. On your own screen you keep looking where you want.

**Category:** Fun
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Yaw | Mode Selector | Random | Static, Offset, Random, Jitter, Spin | How your head turns left and right. |
| Yaw → Static → Yaw | Decimal | 0.0 | -180.0..180.0 ° | The direction your head always faces. |
| Yaw → Offset → Offset | Decimal | 0.0 | -180.0..180.0 ° | How far your head is turned away from where you look. |
| Yaw → Jitter → ForwardTicks | Integer | 2 | 0..100 ticks | How long your head faces forward, in ticks (20 per second). |
| Yaw → Jitter → BackwardTicks | Integer | 2 | 0..100 ticks | How long your head faces backward. |
| Yaw → Spin → Speed | Integer | 50 | -70..70 °/tick | How fast your head spins. Negative values spin the other way. |
| Pitch | Mode Selector | Random | Static, Offset, Random | How your head moves up and down. |
| Pitch → Static → Pitch | Decimal | -90.0 | -180.0..180.0 ° | The up or down angle your head always has. |
| Pitch → Offset → Offset | Decimal | 0.0 | -180.0..180.0 ° | How far up or down your head is turned away from where you look. |
| SafePitch | Toggle | true |  | Keeps your head between straight up and straight down, so it never bends in an impossible way. |
| NotDuringSprint | Toggle | true |  | Stops derping while you sprint. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/fun/ModuleDerp.kt)*
