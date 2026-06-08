## ItemChams

ItemChams applies custom visual effects to the items you hold in your hands. It gives your held items a distinctive glowing or tinted appearance, making them stand out visually — useful for personalizing your client's look or improving item visibility during gameplay.

The **Lightmap** group replaces the normal lighting applied to your held item with a custom glow effect. You can control the blend color overlaid on the item, its base transparency, a secondary glow color, and how many glow layers are stacked on top of each other. The layer size and falloff values let you dial in whether the glow is tight and sharp or wide and diffuse.

The **Shield** group lets you tint the shield you're holding. In **Multiply** mode your chosen color is blended with the shield's existing colors, while **Override** mode replaces the shield's color entirely with your chosen tint — handy for making your shield match a theme or simply stand out from the default appearance.

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

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleItemChams.kt)*
