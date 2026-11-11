## Reach

Reach lets you hit entities and break or place blocks from farther away than normal. Entity reach and block reach are set on their own, so you can raise one and leave the other alone.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Entity | Setting Group | | | See [Range](/docs/modules/shared-settings/range). |
| Entity → RangeIncrease | Decimal | 1.0 | 0.0..5.0 blocks | Extra blocks added to how far you can hit entities. |
| Entity → ThroughWallsRange | Decimal | 0.0 | 0.0..8.0 blocks | How far you can hit entities you cannot see. |
| BlockRangeIncrease | Decimal | 0.5 | 0.0..64.0 | Extra blocks added to how far you can reach blocks. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleReach.kt)*
