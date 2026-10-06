## Derp

Derp is a purely cosmetic [Fun](/docs/modules/fun/derp) module that constantly changes the head rotation other players see, so your character appears to look around wildly, stare straight down, or spin in place — all while you keep playing normally. It only affects how your head is presented to the server and nearby players; it does not change where you are actually aiming on your own screen.

Use the **Yaw** selector to control horizontal head movement and the **Pitch** selector for vertical (up/down) movement. By default both are set to **Random**, giving a chaotic, twitchy look. Other modes let you lock to a fixed angle, add an offset to your real view, jitter back and forth, or continuously spin.

Keep **SafePitch** enabled to avoid impossible up/down angles that look obviously fake, and leave **NotDuringSprint** on so the derping pauses while you sprint (handy if you don't want it interfering during movement). For more silly cosmetic effects, pair it with [SkinDerp](/docs/modules/fun/skinderp), [HandDerp](/docs/modules/fun/handderp), or [Twerk](/docs/modules/fun/twerk).

**Category:** Fun
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Yaw | Mode Selector | Random | Static, Offset, Random, Jitter, Spin | How your horizontal (left/right) head rotation behaves. |
| Yaw → [Static] → Yaw | Decimal | 0.0° | -180.0..180.0° | Fixed yaw angle to hold. |
| Yaw → [Offset] → Offset | Decimal | 0.0° | -180.0..180.0° | Amount added to your real yaw. |
| Yaw → [Jitter] → ForwardTicks | Integer | 2 ticks | 0..100 ticks | How many ticks the head faces forward before flipping. |
| Yaw → [Jitter] → BackwardTicks | Integer | 2 ticks | 0..100 ticks | How many ticks the head faces backward before flipping. |
| Yaw → [Spin] → Speed | Integer | 50°/tick | -70..70°/tick | How fast (and which direction) the head spins each tick. |
| Pitch | Mode Selector | Random | Static, Offset, Random | How your vertical (up/down) head rotation behaves. |
| Pitch → [Static] → Pitch | Decimal | -90.0° | -180.0..180.0° | Fixed pitch angle to hold. |
| Pitch → [Offset] → Offset | Decimal | 0.0° | -180.0..180.0° | Amount added to your real pitch. |
| SafePitch | Toggle | Yes | — | Keeps pitch within a realistic -90° to 90° range so it doesn't look obviously fake. |
| NotDuringSprint | Toggle | Yes | — | Pauses the derping while you are sprinting. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/fun/ModuleDerp.kt)*
