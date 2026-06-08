## BlockIn

BlockIn automatically walls you in by placing blocks around your body, sealing you off from your surroundings. Turn it on when you need an instant cover — for example to break line of sight, block incoming projectiles, or buy yourself time during a fight — and the module builds a box that encloses the space you're standing in.

When enabled, it snapshots your current block position and figures out every spot that needs a block: the floor below you, the columns around you up to your full height, and the ceiling above your head, as computed in [the Normal placement order](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBlockIn.kt#L59-L73). The surrounding sides are walked starting from the direction you're facing, rotating either clockwise or counter-clockwise (chosen at random each time it enables). The shared Placer then handles the actual placing, rotations, and timing.

The module is protective about its state: if you move out of your starting position (or the block directly above it) before it finishes, it cancels and notifies you, as seen in [the movement guard](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBlockIn.kt#L149-L157). It also picks hotbar slots intelligently — favoring tougher blocks for the box positions and weaker ones elsewhere — via [the slot finder](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBlockIn.kt#L159-L170). With AutoDisable on, it turns itself off and reports "filled" once the box is complete.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Placer | Setting Group | — | — | See [Shared: Block Placer](/docs/modules/shared-settings/block-placer). |
| AutoDisable | Toggle | true | — | When the box is fully built, sends a "filled" notification and turns the module off automatically. |
| PlaceOrder | Choice | Normal | Normal, Random, BottomTop, TopBottom | Order in which the surrounding positions are placed: Normal uses the natural floor-sides-ceiling sequence, Random shuffles it, BottomTop places lowest blocks first, and TopBottom places highest blocks first. |
| Filter | Choice | Blacklist | Whitelist, Blacklist | How the Blocks list is interpreted. Whitelist places only the listed blocks; Blacklist places anything except the listed blocks. |
| Blocks | Registry List | — | — | The set of blocks used together with Filter to decide which items in your hotbar and offhand are eligible to be placed. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBlockIn.kt)*
