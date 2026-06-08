## ProtectionZones

ProtectionZones renders the coverage area of protection blocks — emerald blocks by default — as coloured boxes overlaid on the world. When enabled, the module scans loaded chunks for any blocks in the **ProtectionBlocks** list and draws an outlined box around each one representing its protected area, using the configured X/Z/Y radius. A zone you are standing inside is shown with just its outline; a zone you are standing close to (but outside, within roughly 5 blocks of the boundary) is highlighted with a coloured fill so gaps in coverage are immediately obvious.

When you are holding a protection block in your main hand or offhand, the module also shows a **placement indicator**: a highlighted single-block position showing exactly where to place your next protection block so that its zone tiles seamlessly with the nearest existing one. The indicator snaps to a grid derived from your configured radius, eliminating guesswork about spacing. Enable **SnapToY** if you want the indicator to match the Y level of the nearest protection block rather than your own current height.

To keep performance reasonable, only the nearest zones up to **RenderLimit** are drawn. If you want the overlay to appear only while you are actively placing blocks, turn on **HoldBlockToRender** — this suppresses the entire render until you pick up a protection block.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ProtectionBlocks | Registry List | — | — | The blocks that define protection zones. The module scans chunks for these blocks and uses them as zone centres. |
| ProtectionRadius | Setting Group | — | — | Controls how far each protection block's zone extends from its centre. |
| ProtectionRadius → RadiusX | Integer | 20 | 1..256 blocks | Zone half-width in the X direction. |
| ProtectionRadius → RadiusZ | Integer | 20 | 1..256 blocks | Zone half-width in the Z direction. |
| ProtectionRadius → RadiusY | Integer | 383 | 1..383 blocks | Zone half-height in the Y direction. |
| PlacementIndicator | Setting Group | — | — | Settings for the optimal placement suggestion indicator shown while holding a protection block. |
| PlacementIndicator → SnapToY | Toggle | false | — | When enabled, the indicator's Y position snaps to the nearest protection block's Y level rather than following your own. |
| Renderer | Setting Group | — | — | Controls rendering behaviour, zone count limits, and colours. |
| Renderer → RenderLimit | Integer | 16 | 3..50 zones | Maximum number of zones rendered at once. Only the nearest zones (by horizontal distance) are chosen. |
| Renderer → HoldBlockToRender | Toggle | false | — | When enabled, the entire overlay is hidden unless you are holding a protection block in your main hand or offhand. |
| Renderer → ProtectionColors | Setting Group | — | — | Colour settings applied to the protection zone boxes. |
| Renderer → ProtectionColors → ZoneFill | Color | — | — | Fill colour used on the zone box when you are standing near (but outside) that zone. |
| Renderer → ProtectionColors → ZoneOutline | Color | — | — | Outline colour drawn around each protection zone box. |
| Renderer → ProtectionColors → CenterZoneOutline | Color | — | — | Outline colour drawn around the individual block at the centre of each zone. |
| Renderer → IndicatorColors | Setting Group | — | — | Colour settings for the placement indicator block highlight. |
| Renderer → IndicatorColors → IndicatorOutline | Color | — | — | Outline colour for the placement indicator. |
| Renderer → IndicatorColors → IndicatorFill | Color | — | — | Fill colour for the placement indicator. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleProtectionZones.kt)*
