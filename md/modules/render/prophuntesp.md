## ProphuntESP

ProphuntESP helps you locate hidden props on Prophunt servers by highlighting positions where disguised players are likely to be. In Prophunt, players disguise themselves as blocks or objects — but when they move, they reveal themselves through falling-block entities and block update packets sent by the server. This module listens for those telltale signals and renders a highlight over the affected positions so you can track them down.

You can choose which types of events to watch: **FallingBlocks** tracks entities that are physically falling through the air (a common giveaway when a prop jumps or drops), **BlockUpdates** catches single-block change packets (triggered when a prop swaps disguise or moves in place), and **ChunkDeltaUpdates** catches bulk multi-block change packets that cover the same behaviour across a wider area. All three are enabled by default for maximum coverage. The highlights are rendered using the **RenderBlockUpdates** group, which you can customise or disable entirely if you only want detection without a visual overlay.

This module is purely passive — it does not interact with or attack other players. Use it alongside [ESP](/docs/modules/render/esp) or [Tracers](/docs/modules/render/tracers) for a fuller picture of where players are hiding.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Tracking | Multi-Select | FallingBlocks, BlockUpdates, ChunkDeltaUpdates | FallingBlocks, BlockUpdates, ChunkDeltaUpdates | Which event types to monitor for hidden props. Select any combination of falling-block entities, single block update packets, and chunk-section (multi-block) update packets. |
| RenderBlockUpdates | Toggleable Group | on | — | See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering) |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleProphuntESP.kt)*
