## HandDerp

HandDerp is a cosmetic prank module that rapidly flips your main hand back and forth between left and right. The result is a jittery, "derping" look as your held item and arm constantly swap sides — purely for fun, with no impact on combat or movement. Like [Derp](/docs/modules/fun/derp), [SkinDerp](/docs/modules/fun/skinderp), and [Twerk](/docs/modules/fun/twerk), it's meant to mess around and make your character look silly.

The **Silent** option keeps the hand-swapping visible to other players on the server while hiding the flicker on your own screen, so you don't have to watch the constant switching yourself. Choose how the swaps are triggered with **Mode**: **Delay** flips your hand on a fixed timer, while **Swing** flips it every time you swing your arm (for example when attacking or breaking blocks). When you turn the module off, your main hand is automatically restored to its original side.

**Category:** Fun
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Silent | Toggle | false | — | Hides the hand-switching from your own view while still sending it to the server. |
| Mode | Mode Selector | Delay | Delay, Swing | How hand swaps are triggered. |
| Mode → [Delay] → Delay | Integer | 1 | 0..20 ticks | How long to wait between each hand swap. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/fun/ModuleHandDerp.kt)*
