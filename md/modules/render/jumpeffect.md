## JumpEffect

JumpEffect draws a ring on the ground under you every time you jump. It grows and fades out quickly. It is only for looks.

**Simple** draws a colored ring. **Image** draws a picture on the ground instead, either one that comes with the client or your own, and can spin it. The colors can shift while the effect plays, which makes a rainbow-like sweep.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Simple | Simple, Image | Draw a ring or a picture. |
| Mode → (all) → EndRadius | Decimal Range | 0.15 to 0.8 | 0.0 to 3.0 | The inner and outer size the effect grows to. |
| Mode → (all) → AnimCurve | Choice | QuadOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the growing speeds up or slows down. |
| Mode → (all) → HueOffsetAnim | Integer | -63 | -360 to 360 | How far the color shifts while the effect plays. 0 keeps the color the same. |
| Mode → (all) → Lifetime | Integer Range | 15 to 15 | 1 to 120 | How long the effect grows, then how long until it is gone, in ticks (20 per second). |
| Mode → (all) → CanBeCovered | Toggle | false | | Lets blocks hide the effect. When off, it is always drawn on top. |
| Mode → (all) → Colors → InnerColor | Color | LiquidBounce blue, alpha 50 | | Color in the middle. |
| Mode → (all) → Colors → OuterColor | Color | LiquidBounce blue, alpha 150 | | Color at the edge. |
| Mode → Simple → Render | Choice | Plain | Plain, Shader | **Plain** draws the ring normally. **Shader** draws it with a shader effect, and its **Style** setting picks how that looks. |
| Mode → Image → RotationSpeed | Integer | 10 | -360 to 360 | How fast the picture spins. 0 keeps it still. |
| Mode → Image → Source | Mode Selector | Builtin | Builtin, Custom | Use a picture from the client or your own file. |
| Mode → Image → Source → Builtin → Preset | Choice | LiquidBounce | LiquidBounce, LiquidBounceWithLogo | Which built-in picture to use. |
| Mode → Image → Source → Custom → File | File | | PNG, JPG | Your own picture. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/jumpeffect/ModuleJumpEffect.kt)*
