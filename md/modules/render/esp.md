## ESP

ESP (Extra Sensory Perception) highlights living entities like players and mobs so you can spot them through walls and across the map. It's one of the most useful render features for keeping track of who's around you, whether you're fighting, hiding, or just exploring.

You can choose how targets are drawn with the **Mode** setting: a 3D **Box** around each entity, a screen-aligned **2D** box with optional health bar, the classic **Legacy2D** marker, or **Glow**, which gives entities a vanilla glowing outline. The **ColorMode** setting controls how those highlights are colored — by distance, by remaining health, a single static color, or a shifting rainbow. On top of that, invisible entities and [friends](/docs/modules/misc/teams) get their own dedicated colors, and entities that were just hit briefly flash red.

The **Glow** modes rely on entities being rendered, so to see hidden or invisible targets through walls with those modes you'll want [TrueSight](/docs/modules/render/truesight). For filled-in or recolored entity models instead of boxes, see [Chams](/docs/modules/render/chams), and use [Nametags](/docs/modules/render/nametags) to label them. Use **MaximumDistance** to limit how far away entities are still drawn.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | 2D | Box, 2D, Legacy2D, Glow | How entities are highlighted on screen. |
| Mode → [Box] → Expand | Decimal | 0.05 | 0.0..0.5 | Grows the box outward from the entity. |
| Mode → [Box] → Outline | Toggle | true | — | Draws an outline around the box. |
| Mode → [Box] → MergeIntersecting | Toggle | false | — | Combines overlapping boxes into one shape. |
| Mode → [2D] → Expand | Decimal | 0.05 | 0.0..0.5 | Grows the box outward from the entity. |
| Mode → [2D] → Fill | Toggle | true | — | Fills the 2D box with a translucent color. |
| Mode → [2D] → Outline | Toggleable Group | On | — | Draws an outline around the 2D box. |
| Mode → [2D] → Outline → Thickness | Decimal | 1.0 | 1.0..9.0 px | Width of the outline. |
| Mode → [2D] → Corner | Toggleable Group | Off | — | Draws only the corners of the box instead of full edges. |
| Mode → [2D] → Corner → Gap | Decimal | 50.0 | 1.0..100.0 % | Size of the open gap between corners. |
| Mode → [2D] → Border | Toggleable Group | On | — | Adds a black border around the outline for contrast. |
| Mode → [2D] → Border → Thickness | Decimal | 1.0 | 1.0..9.0 px | Width of the border. |
| Mode → [2D] → HealthBar | Toggleable Group | On | — | Shows a health bar next to the box. |
| Mode → [2D] → HealthBar → Spacing | Decimal | 2.0 | 0.0..32.0 px | Distance between the box and the health bar. |
| Mode → [Legacy2D] → Scale | Decimal | 0.1 | 0.02..0.3 | Size of the legacy marker. |
| Mode → [Legacy2D] → YOffset | Decimal | 0.0 | -1.0..1.0 | Moves the marker up or down. |
| Mode → [Legacy2D] → BackgroundAlpha | Integer | 150 | 0..255 | Opacity of the marker's background. |
| ColorMode | Mode Selector | Health | Distance, Health, Static, Rainbow | How highlights are colored. |
| ColorMode → [Distance] → Saturation | Decimal | 1.0 | 0.0..1.0 | Color saturation based on distance. |
| ColorMode → [Distance] → Brightness | Decimal | 1.0 | 0.0..1.0 | Color brightness based on distance. |
| ColorMode → [Distance] → Hue | Curve | — | — | Maps distance to a hue along a custom curve. |
| ColorMode → [Distance] → Alpha | Decimal | 1.0 | 0.0..1.0 | Opacity of the color. |
| ColorMode → [Health] → Alpha | Integer | 255 | 0..255 | Opacity of the health-based color. |
| ColorMode → [Static] → Color | Color | — | — | The single color applied to all entities. |
| Invisible | Color | — | — | Color used for invisible entities. |
| Friends | Color | — | — | Color used for friends. |
| MaximumDistance | Decimal | 128.0 | 1.0..512.0 | Maximum distance at which entities are highlighted. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/esp/ModuleESP.kt)*
