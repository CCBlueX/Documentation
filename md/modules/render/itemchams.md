## ItemChams

ItemChams applies custom visual effects to the items you hold in your hands. It gives your held items a distinctive glowing or tinted appearance, making them stand out visually — useful for personalizing your client's look or improving item visibility during gameplay.

The **Lightmap** group replaces the normal lighting applied to your held item with a custom glow effect. You can control the blend color overlaid on the item, its base transparency, a secondary glow color, and how many glow layers are stacked on top of each other. The layer size and falloff values let you dial in whether the glow is tight and sharp or wide and diffuse.

The **Shield** group lets you tint the shield you're holding. In **Multiply** mode your chosen color is blended with the shield's existing colors, while **Override** mode replaces the shield's color entirely with your chosen tint — handy for making your shield match a theme or simply stand out from the default appearance.

The **Effects** group composes additional screen-space layers on top of the held item, each of which can be toggled on its own. **Flow** sweeps an animated pattern across the item, **Trail** leaves a fading afterimage behind it as it moves, **Glow** adds an outline-style halo around its silhouette, **Chromatic** splits the color channels apart for an aberration look, **Scanlines** overlays moving stripes, and **Recolor** animates the item's own hue, saturation and brightness instead of adding a layer. Combining several of them gives the item a more elaborate appearance than the lightmap glow alone.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Lightmap | Toggleable Group | on | — | Applies a custom glow/lightmap effect to held items. |
| Lightmap → BlendColor | Color | — | — | The primary color blended over the item's lightmap. |
| Lightmap → Alpha | Integer | 95 | 1–255 | Overall opacity of the lightmap blend effect. |
| Lightmap → GlowColor | Color | — | — | The secondary color used for the outer glow layers. |
| Lightmap → Layers | Integer | 3 | 1–10 | Number of glow layers rendered on top of the item. |
| Lightmap → LayerSize | Decimal | 1.91 | 1.0–5.0 | Size multiplier for each glow layer. |
| Lightmap → Falloff | Decimal | 6.83 | 0.0–20.0 | How quickly the glow fades out from the item's edges. |
| Shield | Toggleable Group | on | — | Applies a color tint to your held shield. |
| Shield → TintMode | Choice | Multiply | — | How the tint color is applied: **Override** replaces the shield's color entirely; **Multiply** blends it with the existing colors. |
| Shield → Tint | Color | — | — | The color used to tint the shield. |
| Effects | Toggleable Group | off | — | Composes additional screen-space effect layers over the held item. |
| Effects → Flow | Toggleable Group | on | — | Sweeps an animated flowing pattern across the item. |
| Effects → Flow → Color | Color | — | — | Color of the flowing pattern. |
| Effects → Flow → Speed | Decimal | 0.6 | 0.0–5.0 | How fast the pattern moves. |
| Effects → Flow → Scale | Decimal | 12.0 | 1.0–64.0 | Size of the pattern. |
| Effects → Flow → Sharpness | Decimal | 6.0 | 1.0–64.0 | How hard the edges of the pattern are. |
| Effects → Flow → Angle | Decimal | 45 | 0–360° | Direction in which the pattern travels. |
| Effects → Flow → Intensity | Decimal | 0.8 | 0.0–4.0 | Strength of the flow layer. |
| Effects → Trail | Toggleable Group | on | — | Leaves a fading afterimage of the item behind its movement. |
| Effects → Trail → Color | Color | — | — | Color of the trail. |
| Effects → Trail → Weight | Decimal | 0.7 | 0.0–4.0 | How strongly each frame is added to the trail. |
| Effects → Trail → Decay | Decimal | 0.86 | 0.0–1.0 | How much of the previous trail is kept each frame; higher values make longer trails. |
| Effects → Trail → Drift | Vector2_f | 2, 0 | — | Direction and distance the trail drifts as it fades. |
| Effects → Glow | Toggleable Group | off | — | Draws a halo around the item's silhouette. |
| Effects → Glow → Color | Color | — | — | Color of the halo. |
| Effects → Glow → Radius | Decimal | 6 | 1–32 px | How far the halo extends from the silhouette. |
| Effects → Glow → Thickness | Decimal | 1.5 | 0.2–8.0 | Thickness of the halo band. |
| Effects → Glow → Intensity | Decimal | 0.9 | 0.0–4.0 | Strength of the halo. |
| Effects → Chromatic | Toggleable Group | off | — | Splits the color channels apart for a chromatic aberration look. |
| Effects → Chromatic → Strength | Decimal | 2 | 0–16 px | How far the channels are offset from each other. |
| Effects → Chromatic → Ghost | Toggle | off | — | Keeps the offset channels as visible ghost copies of the item. |
| Effects → Scanlines | Toggleable Group | off | — | Overlays moving stripes across the item. |
| Effects → Scanlines → Color | Color | — | — | Color of the stripes. |
| Effects → Scanlines → Spacing | Decimal | 40 | 2–256 px | Distance between two stripes. |
| Effects → Scanlines → Thickness | Decimal | 0.4 | 0.02–1.0 | Width of each stripe relative to the spacing. |
| Effects → Scanlines → Speed | Decimal | 0.3 | -5.0–5.0 | How fast the stripes move; negative values reverse the direction. |
| Effects → Scanlines → Angle | Decimal | 90 | 0–360° | Orientation of the stripes. |
| Effects → Scanlines → Intensity | Decimal | 0.5 | 0.0–4.0 | Strength of the stripe layer. |
| Effects → Recolor | Toggleable Group | off | — | Animates the item's own colors instead of adding a layer. |
| Effects → Recolor → HueSpeed | Decimal | 0.2 | -2.0–2.0 | How fast the hue cycles; negative values cycle backwards. |
| Effects → Recolor → HueMix | Decimal | 1.0 | 0.0–1.0 | How much of the shifted hue replaces the item's original hue. |
| Effects → Recolor → Saturation | Decimal | 1.4 | 0.0–3.0 | Saturation multiplier applied to the item. |
| Effects → Recolor → Brightness | Decimal | 1.2 | 0.0–3.0 | Brightness multiplier applied to the item. |
| Effects → Recolor → PulseSpeed | Decimal | 2.0 | 0.0–12.0 | How fast the brightness pulses. |
| Effects → Recolor → PulseAmount | Decimal | 0.15 | 0.0–1.0 | How strongly the brightness pulses. |

---
*Last updated: 2026-10-11 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleItemChams.kt)*
