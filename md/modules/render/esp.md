## ESP

ESP highlights players and mobs so you can see them through walls and from far away.

**Mode** picks how they are drawn: **Box** puts a 3D box around them, **2D** a flat box with a health bar, **Legacy2D** an older marker, and **Glow** draws a glow around their outline. Glow also shows invisible players and mobs. In Glow mode, **Style** picks how the glow looks. **Vanilla** is the normal Minecraft glow, the other styles are effects with their own settings.

**ColorMode** picks the color: by distance, by health, one fixed color, or a rainbow. Friends and invisible entities get their own colors. To label entities, use [Nametags](/docs/modules/render/nametags). To color the entity itself, use [Chams](/docs/modules/render/chams).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Glow | Box, 2D, Legacy2D, Glow | How entities are highlighted. |
| Mode → Box → Expand | Decimal | 0.05 | 0.0 to 0.5 | Makes the box bigger than the entity. |
| Mode → Box → Outline | Toggle | true | | Draws an outline around the box. |
| Mode → Box → MergeIntersecting | Toggle | false | | Joins boxes that overlap into one shape. |
| Mode → 2D → Expand | Decimal | 0.05 | 0.0 to 0.5 | Makes the box bigger than the entity. |
| Mode → 2D → Outline | Toggleable Group | On | | Draws an outline around the box. |
| Mode → 2D → Outline → Thickness | Decimal | 1.0 | 1.0 to 9.0 px | How thick the outline is. |
| Mode → 2D → Corner | Toggleable Group | Off | | Only draws the corners of the box. |
| Mode → 2D → Corner → Gap | Decimal | 50.0 | 1.0 to 100.0 % | How big the gap between the corners is. |
| Mode → 2D → Border | Toggleable Group | On | | Adds a black border around the outline so it is easier to see. |
| Mode → 2D → Border → Thickness | Decimal | 1.0 | 1.0 to 9.0 px | How thick the border is. |
| Mode → 2D → Fill | Toggle | true | | Fills the box with see-through color. |
| Mode → 2D → HealthBar | Toggleable Group | On | | Shows a health bar next to the box. |
| Mode → 2D → HealthBar → Spacing | Decimal | 2.0 | 0.0 to 32.0 px | Space between the box and the health bar. |
| Mode → Legacy2D → Scale | Decimal | 0.1 | 0.02 to 0.3 | Size of the marker. |
| Mode → Legacy2D → YOffset | Decimal | 0.0 | -1.0 to 1.0 | Moves the marker up or down. |
| Mode → Legacy2D → BackgroundAlpha | Integer | 150 | 0 to 255 | How see-through the marker's background is. |
| Mode → Glow → Style | Mode Selector | Smooth | Vanilla, Smooth, Outline, Neon, Rainbow, Ripple, Hologram, Halftone, Chromatic, Aura | How the glow looks. |
| Mode → Glow → Style → (all except Vanilla) → Opacity | Decimal | 1.0 | 0.0 to 1.0 | How strong the glow is. |
| Mode → Glow → Style → Smooth → Radius | Decimal | 6.0 | 1.0 to 32.0 px | How far the glow reaches. |
| Mode → Glow → Style → Smooth → Falloff | Decimal | 1.6 | 0.5 to 4.0 | How fast the glow fades. |
| Mode → Glow → Style → Smooth → Intensity | Decimal | 1.0 | 0.0 to 2.0 | How bright the glow is. |
| Mode → Glow → Style → Smooth → Fill | Decimal | 0.12 | 0.0 to 1.0 | How much the entity itself is colored in. |
| Mode → Glow → Style → Outline → Width | Decimal | 2.0 | 0.5 to 8.0 px | How thick the outline is. |
| Mode → Glow → Style → Outline → Softness | Decimal | 1.0 | 0.1 to 4.0 px | How soft the outline's edge is. |
| Mode → Glow → Style → Outline → GlowRadius | Decimal | 6.0 | 0.0 to 24.0 px | How far the glow around the outline reaches. |
| Mode → Glow → Style → Outline → GlowIntensity | Decimal | 0.35 | 0.0 to 1.0 | How bright that glow is. |
| Mode → Glow → Style → Outline → Fill | Decimal | 0.0 | 0.0 to 1.0 | How much the entity itself is colored in. |
| Mode → Glow → Style → Neon → CoreColor | Color | White | | Color of the bright line in the middle. |
| Mode → Glow → Style → Neon → CoreMix | Decimal | 0.7 | 0.0 to 1.0 | How much of the core color is used. |
| Mode → Glow → Style → Neon → CoreWidth | Decimal | 1.5 | 0.5 to 6.0 px | How thick the bright line is. |
| Mode → Glow → Style → Neon → BloomRadius | Decimal | 12.0 | 1.0 to 32.0 px | How far the glow reaches. |
| Mode → Glow → Style → Neon → BloomIntensity | Decimal | 1.2 | 0.0 to 3.0 | How bright the glow is. |
| Mode → Glow → Style → Neon → Fill | Decimal | 0.08 | 0.0 to 1.0 | How much the entity itself is colored in. |
| Mode → Glow → Style → Neon → PulseSpeed | Decimal | 0.5 | 0.0 to 4.0 Hz | How fast the glow pulses. |
| Mode → Glow → Style → Neon → PulseAmount | Decimal | 0.25 | 0.0 to 1.0 | How strong the pulsing is. |
| Mode → Glow → Style → Rainbow → Width | Decimal | 2.0 | 0.5 to 8.0 px | How thick the outline is. |
| Mode → Glow → Style → Rainbow → GlowRadius | Decimal | 6.0 | 0.0 to 24.0 px | How far the glow reaches. |
| Mode → Glow → Style → Rainbow → GlowIntensity | Decimal | 0.5 | 0.0 to 1.0 | How bright the glow is. |
| Mode → Glow → Style → Rainbow → Fill | Decimal | 0.1 | 0.0 to 1.0 | How much the entity itself is colored in. |
| Mode → Glow → Style → Rainbow → Speed | Decimal | 0.35 | -2.0 to 2.0 | How fast the colors move. Below 0 they move the other way. |
| Mode → Glow → Style → Rainbow → Spread | Decimal | 400.0 | 50.0 to 2000.0 px | How wide one full rainbow is. |
| Mode → Glow → Style → Rainbow → Saturation | Decimal | 0.85 | 0.0 to 1.0 | How strong the colors are. |
| Mode → Glow → Style → Rainbow → EntityMix | Decimal | 0.0 | 0.0 to 1.0 | How much of the entity's ESP color is mixed in. |
| Mode → Glow → Style → Ripple → Reach | Decimal | 28.0 | 4.0 to 64.0 px | How far the rings go. |
| Mode → Glow → Style → Ripple → Spacing | Decimal | 10.0 | 3.0 to 32.0 px | Space between rings. |
| Mode → Glow → Style → Ripple → RingWidth | Decimal | 2.0 | 0.5 to 8.0 px | How thick each ring is. |
| Mode → Glow → Style → Ripple → Speed | Decimal | 16.0 | -64.0 to 64.0 px/s | How fast the rings move. |
| Mode → Glow → Style → Ripple → EdgeWidth | Decimal | 1.5 | 0.0 to 6.0 px | How thick the outline is. |
| Mode → Glow → Style → Ripple → Fill | Decimal | 0.08 | 0.0 to 1.0 | How much the entity itself is colored in. |
| Mode → Glow → Style → Hologram → StripeColor | Color | White | | Color of the stripes. |
| Mode → Glow → Style → Hologram → Stripes | Decimal | 0.55 | 0.0 to 1.0 | How visible the stripes are. |
| Mode → Glow → Style → Hologram → Spacing | Decimal | 6.0 | 2.0 to 32.0 px | Space between stripes. |
| Mode → Glow → Style → Hologram → Angle | Decimal | 90.0 | 0.0 to 180.0 ° | Angle of the stripes. |
| Mode → Glow → Style → Hologram → Speed | Decimal | 1.0 | -8.0 to 8.0 | How fast the stripes move. |
| Mode → Glow → Style → Hologram → Fill | Decimal | 0.18 | 0.0 to 1.0 | How much the entity itself is colored in. |
| Mode → Glow → Style → Hologram → EdgeWidth | Decimal | 1.5 | 0.5 to 6.0 px | How thick the outline is. |
| Mode → Glow → Style → Hologram → Flicker | Decimal | 0.15 | 0.0 to 1.0 | How much the effect flickers. |
| Mode → Glow → Style → Halftone → Reach | Decimal | 12.0 | 2.0 to 48.0 px | How far the dots reach. |
| Mode → Glow → Style → Halftone → CellSize | Decimal | 5.0 | 3.0 to 24.0 px | Space between dots. |
| Mode → Glow → Style → Halftone → DotScale | Decimal | 0.9 | 0.2 to 1.5 | Size of the dots. |
| Mode → Glow → Style → Halftone → Fill | Decimal | 0.0 | 0.0 to 1.0 | How much the entity itself is colored in. |
| Mode → Glow → Style → Halftone → EdgeWidth | Decimal | 1.0 | 0.0 to 4.0 px | How thick the outline is. |
| Mode → Glow → Style → Chromatic → Width | Decimal | 2.0 | 0.5 to 8.0 px | How thick the outline is. |
| Mode → Glow → Style → Chromatic → Split | Decimal | 3.0 | 0.0 to 12.0 px | How far the color layers are pulled apart. |
| Mode → Glow → Style → Chromatic → Speed | Decimal | 1.5 | -8.0 to 8.0 rad/s | How fast the layers turn. |
| Mode → Glow → Style → Chromatic → Tint | Decimal | 0.3 | 0.0 to 1.0 | How much of the ESP color is mixed in. |
| Mode → Glow → Style → Chromatic → GlowRadius | Decimal | 3.0 | 0.0 to 16.0 px | How far the glow reaches. |
| Mode → Glow → Style → Chromatic → Fill | Decimal | 0.08 | 0.0 to 1.0 | How much the entity itself is colored in. |
| Mode → Glow → Style → Aura → Radius | Decimal | 6.0 | 2.0 to 32.0 px | How far the aura reaches to the sides. |
| Mode → Glow → Style → Aura → Height | Decimal | 16.0 | 0.0 to 48.0 px | How high the aura rises. |
| Mode → Glow → Style → Aura → Sway | Decimal | 3.0 | 0.0 to 16.0 px | How much the aura sways. |
| Mode → Glow → Style → Aura → Scale | Decimal | 10.0 | 4.0 to 64.0 px | Size of the aura's pattern. |
| Mode → Glow → Style → Aura → Speed | Decimal | 1.5 | 0.0 to 6.0 | How fast the aura moves. |
| Mode → Glow → Style → Aura → Intensity | Decimal | 1.2 | 0.0 to 3.0 | How bright the aura is. |
| Mode → Glow → Style → Aura → Heat | Decimal | 0.3 | 0.0 to 1.0 | How hot and bright the aura's colors look. |
| Mode → Glow → Style → Aura → Fill | Decimal | 0.1 | 0.0 to 1.0 | How much the entity itself is colored in. |
| ColorMode | Mode Selector | Distance | Distance, Health, Static, Rainbow | How the highlight is colored. |
| ColorMode → Distance → Saturation | Decimal | 1.0 | 0.0 to 1.0 | How strong the color is. |
| ColorMode → Distance → Brightness | Decimal | 1.0 | 0.0 to 1.0 | How bright the color is. |
| ColorMode → Distance → Hue | Curve | | Distance 0 to 200, Hue 0 to 360 | Which color is used at which distance. |
| ColorMode → Distance → Alpha | Decimal | 1.0 | 0.0 to 1.0 | How see-through the color is. |
| ColorMode → Health → Alpha | Integer | 255 | 0 to 255 | How see-through the color is. |
| ColorMode → Static → Color | Color | White, alpha 100 | | The color used for every entity. |
| Invisible | Color | Orange | | Color of invisible entities. |
| Friends | Color | Green | | Color of your friends. |
| MaximumDistance | Decimal | 128.0 | 1.0 to 512.0 | How far away entities are still highlighted, in blocks. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/esp/ModuleESP.kt)*
