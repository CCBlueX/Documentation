## JumpEffect

JumpEffect renders a glowing effect on the ground beneath your feet each time you jump. It expands outward and fades away over a short time, adding a stylish visual flourish to your movement without affecting gameplay in any way.

JumpEffect offers two **Mode**s. **Simple** draws the classic gradient ring. **Image** instead draws an image flat on the ground — either one of the images bundled with the client or a file of your own — and can spin it while it plays out.

You can fully customise the look of the effect: change the inner and outer colours, adjust how large it grows, control how long it lingers, and choose an easing curve to shape the expansion animation. The hue shift option lets the colour rotate as the effect plays out, producing a rainbow-like sweep for every jump.

By default the effect always renders on top of blocks — disable **CanBeCovered** to let blocks occlude it for a more grounded look.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Simple | Simple \| Image | How the effect is drawn: a gradient ring or an image. |
| Mode → EndRadius | Decimal Range | 0.15..0.8 | 0.0..3.0 | The inner-to-outer radius range the effect expands to at the end of its animation. |
| Mode → AnimCurve | Choice | QuadOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | Easing curve that controls how the effect expands over its lifetime. |
| Mode → HueOffsetAnim | Integer | 63 | -360..360 | How many degrees to shift the hue across the animation. Set to 0 to disable hue animation. |
| Mode → Lifetime | Integer Range | 15..15 | 1..120 | The first value is how many ticks the expansion animation takes, the second how many ticks pass before the effect has fully faded out. |
| Mode → CanBeCovered | Toggle | false | — | When enabled, blocks in the world can occlude the effect. When disabled, it always renders on top of geometry. |
| Mode → Colors → InnerColor | Color | — | — | Colour at the centre of the gradient. |
| Mode → Colors → OuterColor | Color | — | — | Colour at the outer edge of the gradient. |
| Mode → [Image] → RotationSpeed | Integer | 10 | -360..360 | How fast the image spins while the effect plays out. Set to 0 to keep it still. |
| Mode → [Image] → Source | Mode Selector | Builtin | Builtin \| Custom | Where the image comes from: **Builtin** picks one of the images shipped with LiquidBounce, **Custom** uses an image file you provide. |

---
*Last updated: 2026-08-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/jumpeffect/ModuleJumpEffect.kt)*
