## ItemChams

ItemChams adds glow and color effects to the items in your hands. It only changes how they look to you.

**Lightmap** gives the held item a colored glow. **Shield** tints your shield: **Multiply** mixes your color with the shield's own colors, **Override** replaces them. **Effects** adds extra layers you can turn on one by one: a moving pattern (Flow), a fading trail when the item moves (Trail), a glow around its edge (Glow), split colors (Chromatic), moving stripes (Scanlines) and changing colors (Recolor).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Lightmap | Toggleable Group | On | | Gives held items a colored glow. |
| Lightmap → BlendColor | Color | 0, 64, 255, 186 | | The main color of the glow. |
| Lightmap → Alpha | Integer | 95 | 1 to 255 | How strong the glow is. |
| Lightmap → GlowColor | Color | 0, 64, 255, 15 | | Color of the outer glow layers. |
| Lightmap → Layers | Integer | 3 | 1 to 10 | How many glow layers there are. |
| Lightmap → LayerSize | Decimal | 1.91 | 1.0 to 5.0 | How big each layer is. |
| Lightmap → Falloff | Decimal | 6.83 | 0.0 to 20.0 | How fast the glow fades out. |
| Shield | Toggleable Group | On | | Tints your shield. |
| Shield → TintMode | Choice | Multiply | Override, Multiply | Mix the tint with the shield's colors, or replace them. |
| Shield → Tint | Color | White | | The tint color. |
| Effects | Toggleable Group | Off | | Adds extra effect layers on top of the held item. |
| Effects → Flow | Toggleable Group | On | | A pattern that moves across the item. |
| Effects → Flow → Color | Color | Light accent | | Color of the pattern. |
| Effects → Flow → Speed | Decimal | 0.6 | 0.0 to 5.0 | How fast the pattern moves. |
| Effects → Flow → Scale | Decimal | 12.0 | 1.0 to 64.0 | Size of the pattern. |
| Effects → Flow → Sharpness | Decimal | 6.0 | 1.0 to 64.0 | How sharp the pattern's edges are. |
| Effects → Flow → Angle | Decimal | 45.0 | 0.0 to 360.0 ° | Which way the pattern moves. |
| Effects → Flow → Intensity | Decimal | 0.8 | 0.0 to 4.0 | How strong the pattern is. |
| Effects → Trail | Toggleable Group | On | | Leaves a fading trail behind the item when it moves. |
| Effects → Trail → Color | Color | LiquidBounce blue | | Color of the trail. |
| Effects → Trail → Weight | Decimal | 0.7 | 0.0 to 4.0 | How strong the trail is. |
| Effects → Trail → Decay | Decimal | 0.86 | 0.0 to 1.0 | How long the trail stays. Higher means a longer trail. |
| Effects → Trail → Drift | Vector | 2, 0 | | Which way the trail moves while it fades. |
| Effects → Glow | Toggleable Group | Off | | A glow around the item's edge. |
| Effects → Glow → Color | Color | Light accent | | Color of the glow. |
| Effects → Glow → Radius | Decimal | 6.0 | 1.0 to 32.0 px | How far the glow reaches. |
| Effects → Glow → Thickness | Decimal | 1.5 | 0.2 to 8.0 | How thick the glow is. |
| Effects → Glow → Intensity | Decimal | 0.9 | 0.0 to 4.0 | How bright the glow is. |
| Effects → Chromatic | Toggleable Group | Off | | Splits the item's colors apart a little. |
| Effects → Chromatic → Strength | Decimal | 2.0 | 0.0 to 16.0 px | How far the colors are pulled apart. |
| Effects → Chromatic → Ghost | Toggle | false | | Shows the split colors as see-through copies of the item. |
| Effects → Scanlines | Toggleable Group | Off | | Moving stripes over the item. |
| Effects → Scanlines → Color | Color | Light accent | | Color of the stripes. |
| Effects → Scanlines → Spacing | Decimal | 40.0 | 2.0 to 256.0 px | Space between stripes. |
| Effects → Scanlines → Thickness | Decimal | 0.4 | 0.02 to 1.0 | How thick each stripe is compared to the space. |
| Effects → Scanlines → Speed | Decimal | 0.3 | -5.0 to 5.0 | How fast the stripes move. Below 0 they move the other way. |
| Effects → Scanlines → Angle | Decimal | 90.0 | 0.0 to 360.0 ° | Which way the stripes point. |
| Effects → Scanlines → Intensity | Decimal | 0.5 | 0.0 to 4.0 | How strong the stripes are. |
| Effects → Recolor | Toggleable Group | Off | | Changes the item's own colors over time. |
| Effects → Recolor → HueSpeed | Decimal | 0.2 | -2.0 to 2.0 | How fast the color changes. Below 0 it goes the other way. |
| Effects → Recolor → HueMix | Decimal | 1.0 | 0.0 to 1.0 | How much the new color replaces the item's own color. |
| Effects → Recolor → Saturation | Decimal | 1.4 | 0.0 to 3.0 | How strong the colors are. |
| Effects → Recolor → Brightness | Decimal | 1.2 | 0.0 to 3.0 | How bright the item is. |
| Effects → Recolor → PulseSpeed | Decimal | 2.0 | 0.0 to 12.0 | How fast the brightness pulses. |
| Effects → Recolor → PulseAmount | Decimal | 0.15 | 0.0 to 1.0 | How strong the pulsing is. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleItemChams.kt)*
