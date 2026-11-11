## ProphuntESP

ProphuntESP helps you find hiding players in Prop Hunt. Players disguised as blocks give themselves away when they move, because the server sends block changes or falling blocks at their spot. This module marks those spots.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Tracking | Multi-Select | FallingBlocks, BlockUpdates, ChunkDeltaUpdates | FallingBlocks, BlockUpdates, ChunkDeltaUpdates | What to watch for. **FallingBlocks** marks falling blocks, **BlockUpdates** marks single blocks that change, **ChunkDeltaUpdates** marks groups of blocks that change at once. At least one must stay on. |
| RenderBlockUpdates | Toggleable Group | on | | How the marked spots look. See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleProphuntESP.kt)*
