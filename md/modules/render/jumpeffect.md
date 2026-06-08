## JumpEffect

JumpEffect renders a glowing gradient ring on the ground beneath your feet each time you jump. The ring expands outward and fades away over a short time, adding a stylish visual flourish to your movement without affecting gameplay in any way.

You can fully customise the look of the effect: change the inner and outer ring colours, adjust how large the ring grows, control how long it lingers, and choose an easing curve to shape the expansion animation. The hue shift option lets the colour rotate as the ring plays out, producing a rainbow-like sweep for every jump.

By default the effect always renders on top of blocks — disable **CanBeCovered** to let blocks occlude it for a more grounded look.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| EndRadius | Decimal Range | 0.15..0.8 | 0.0..3.0 | The inner-to-outer radius range the ring expands to at the end of its animation. |
| InnerColor | Color | — | — | Colour at the centre of the gradient ring. |
| OuterColor | Color | — | — | Colour at the outer edge of the gradient ring. |
| AnimCurve | Choice | QuadOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | Easing curve that controls how the ring expands over its lifetime. |
| HueOffsetAnim | Integer | 63 | -360..360 | How many degrees to shift the hue across the animation. Set to 0 to disable hue animation. |
| Lifetime | Integer | 15 | 1..30 | How many ticks the ring stays visible before fully fading out. |
| CanBeCovered | Toggle | false | — | When enabled, blocks in the world can occlude the ring. When disabled, the ring always renders on top of geometry. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleJumpEffect.kt)*
