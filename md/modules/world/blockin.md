## BlockIn

BlockIn puts blocks all around you: under your feet, on every side and over your head. Turn it on when you need cover fast, for example to hide from arrows or to get a break in a fight.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Placer | Setting Group | | | See [Block Placer](/docs/modules/shared-settings/block-placer). |
| DisableOn | Multi-Select | Finish, Move | Finish, Move | Finish: turns off when the box is done. Move: turns off when you walk out of your spot. |
| AvoidBrokenBlocks | Toggle | true | | Doesn't place blocks back where you just broke one yourself. |
| BrokenBlockWindow | Integer | 1000 | 0..10000 ms | How long a spot you broke is skipped. |
| PlaceOrder | Choice | Normal | Normal, Random, BottomTop, TopBottom | The order the blocks go down in. BottomTop starts at the bottom, TopBottom at the top. |
| Filter | Choice | Blacklist | Whitelist, Blacklist | Whitelist: only use the listed blocks. Blacklist: use any block except the listed ones. |
| Blocks | Registry List | | | The blocks the filter uses. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBlockIn.kt)*
