## ItemESP

ItemESP highlights dropped items and collectible projectiles in the world, making them visible through terrain and at a distance. It is useful for quickly spotting valuable loot on the ground, tracking arrows you have fired, or locating tridents before they despawn.

You can control exactly which items are highlighted using the **Filter** setting in combination with the **Items** list — set the filter to **Whitelist** to show only the items you add, or leave it on **Blacklist** (the default) to show everything except the items you add. The **MaximumDistance** setting caps how far away an item can be before it stops being highlighted, helping reduce visual clutter on busy servers. Enable **Tracers** to draw a line from your camera to each matching entity, similar to the [Tracers](/docs/modules/render/tracers) module.

Three rendering styles are available: **Glow** applies a soft glow outline, **Box** draws a 3-D bounding box around each item (with an option to merge boxes that overlap), and **Legacy2D** renders a flat 2-D marker above each item whose size and vertical position you can fine-tune. You can also pair ItemESP with [ItemChams](/docs/modules/render/itemchams) for additional item rendering effects.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Filter | Choice | Blacklist | Whitelist, Blacklist | Determines whether the Items list acts as a whitelist (show only listed items) or a blacklist (show everything except listed items). |
| Items | Registry List | — | — | The list of items used by the Filter setting. |
| MaximumDistance | Decimal | 128.0 | 1.0–512.0 | Maximum distance in blocks at which items are highlighted. Items beyond this range are ignored. |
| Tracers | Toggle | false | — | Draws a line from your camera to each highlighted item or projectile. |
| ShowArrows | Toggleable Group | on | — | When enabled, collectible arrows in the world are highlighted according to the sub-settings below. |
| ShowArrows → RegularArrows | Toggle | true | — | Highlights regular collectible arrows. |
| ShowArrows → SpectralArrows | Toggle | true | — | Highlights spectral arrows that are collectible. |
| ShowArrows → ArrowsWithEffects | Toggle | true | — | Highlights tipped (effect-carrying) arrows that are collectible. |
| ShowTridents | Toggle | true | — | Highlights thrown tridents lying in the world. |
| Mode | Mode Selector | Box | Glow, Box, Legacy2D | Rendering style used to highlight items and projectiles. |
| Mode → [Box] → MergeIntersecting | Toggle | false | — | When enabled, overlapping item boxes are merged into a single combined box, reducing clutter when many items are stacked together. |
| Mode → [Legacy2D] → Scale | Decimal | 0.1 | 0.02–0.3 | Size of the 2-D marker rendered above each item. |
| Mode → [Legacy2D] → YOffset | Decimal | 0.0 | -1.0–1.0 | Vertical offset of the 2-D marker relative to the item's position. |
| Mode → [Legacy2D] → BackgroundAlpha | Integer | 150 | 0–255 | Opacity of the dark background behind the 2-D marker. 0 is fully transparent, 255 is fully opaque. |
| ColorMode | Mode Selector | Static | Static, Rainbow | Controls how the highlight colour is determined. |
| ColorMode → [Static] → Color | Color | — | — | The fixed colour used when ColorMode is set to Static. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleItemESP.kt)*
