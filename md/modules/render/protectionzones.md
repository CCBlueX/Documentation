## ProtectionZones

ProtectionZones shows the area each protection block (emerald blocks by default) protects, as a box in the world. Zones you are close to but outside of get filled with color, so you can spot gaps between them.

While you hold a protection block, a marked block shows where to place the next one so its zone lines up with the closest existing zone.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ProtectionBlocks | Registry List | Emerald Block | | Blocks that count as protection blocks. |
| ProtectionRadius → RadiusX | Integer | 20 | 1..256 blocks | How far a zone reaches east and west from its block. |
| ProtectionRadius → RadiusZ | Integer | 20 | 1..256 blocks | How far a zone reaches north and south from its block. |
| ProtectionRadius → RadiusY | Integer | 383 | 1..383 blocks | How far a zone reaches up and down from its block. |
| PlacementIndicator → SnapToY | Toggle | false | | Puts the suggested spot at the height of the closest protection block instead of your own height. |
| Renderer → RenderLimit | Integer | 16 | 3..50 zones | Most zones drawn at once. The closest ones are picked. |
| Renderer → HoldBlockToRender | Toggle | false | | Only shows zones while you hold a protection block. |
| Renderer → ProtectionColors → ZoneFill | Color | | | Fill color for zones you are near but outside of. |
| Renderer → ProtectionColors → ZoneOutline | Color | | | Outline color of each zone. |
| Renderer → ProtectionColors → CenterZoneOutline | Color | | | Outline color of the protection block in the middle of each zone. |
| Renderer → IndicatorColors → IndicatorOutline | Color | | | Outline color of the suggested placement spot. |
| Renderer → IndicatorColors → IndicatorFill | Color | | | Fill color of the suggested placement spot. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleProtectionZones.kt)*
