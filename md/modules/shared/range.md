## Range

The Range settings decide how far a module can reach when it hits or uses an entity. A little more reach helps you hit first, but big values are easy for anticheats to notice.

Used by: [KillAura](/docs/modules/combat/killaura), [Reach](/docs/modules/player/reach).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| RangeIncrease | Decimal | 1.0 | 0.0..5.0 blocks | How much further than normal you can reach. |
| ThroughWallsRange | Decimal | depends on the module | 0.0..8.0 blocks | How far you can reach enemies you can't see because blocks are in the way. 0 means you never hit through blocks. It can't be more than your normal reach. KillAura starts at 3.0, Reach at 0.0. |

KillAura adds **ScanRangeIncrease** (default 2.0..3.0, 0.0..7.0 blocks): how much further than your reach it already looks for enemies.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/range/RangeValueGroup.kt)*
