## TotemEffect

TotemEffect draws an effect on a player whenever their Totem of Undying saves them. **Shockwave** draws a ring that grows outward, **Soul** draws a ghost of the player that floats up. It only changes what you see.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Shockwave | Shockwave, Soul | Which effect to draw. |
| Mode → Lifetime | Integer | 20 | 1 to 200 | How long the effect lasts, in ticks (20 per second). Both modes have this setting. |
| Mode → Fade | Decimal | 0.7 | 0.0 to 1.0 | How far into the effect it starts to fade out. 0.7 means it fades during the last 30%. Both modes have this setting. |
| Mode → AnimCurve | Choice | ExponentialOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the animation speeds up or slows down. Both modes have this setting. |
| Mode → CanBeCovered | Toggle | false | | When on, blocks can hide the effect. When off, it is always drawn on top. Both modes have this setting. |
| Mode → Shockwave → radius | Decimal Range | 2.0..2.2 | 0.1 to 10.0 | Inner and outer size of the ring at its biggest. |
| Mode → Shockwave → Colors → SyncColors | Toggle | false | | Uses the inner color for the outer part as well. |
| Mode → Shockwave → Colors → InnerColor | Color | | | Color of the inside of the ring. |
| Mode → Shockwave → Colors → OuterColor | Color | | | Color of the outside of the ring. |
| Mode → Soul → Halo | Toggle | false | | Adds a halo above the ghost's head. |
| Mode → Soul → YMotion | Toggleable Group | on | | Makes the ghost float upward. |
| Mode → Soul → YMotion → SoulYMotion | Decimal | 0.75 | 0.1 to 10.0 | How fast the ghost rises. |
| Mode → Soul → YMotion → AnimBy | Choice | Age | Progress, Age | **Age** makes the ghost rise at a steady pace. **Progress** follows the AnimCurve. |
| Mode → Soul → Colors → SyncColors | Toggle | false | | Uses the fill color for the outline as well. |
| Mode → Soul → Colors → InnerColor | Color | | | Fill color of the ghost. |
| Mode → Soul → Colors → OuterColor | Color | | | Outline color of the ghost. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/totemeffect/ModuleTotemEffect.kt)*
