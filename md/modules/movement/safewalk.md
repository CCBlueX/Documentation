## SafeWalk

SafeWalk prevents you from accidentally walking off the edge of blocks, mimicking the effect of holding the sneak key without slowing you down. It is useful anywhere precise footing matters: narrow bridges, edge-of-world traversal, parkour setups, or any situation where one wrong step means a long fall.

The module offers two active modes. **Safe** gives you constant sneak-like edge protection whenever the module is on — you simply cannot step off a ledge while it is active. **OnEdge** is more surgical: it watches your movement in real time, and only intervenes when you are actually approaching a drop. When a dangerous edge is detected, OnEdge can stop your momentum, reverse your direction, or steer you back toward the center of the block you are standing on, then releases control once the threat has passed. The **None** option disables any protection while keeping the module toggled on, which is mainly useful when cycling through modes.

If you want the simplest, most reliable protection, **Safe** mode is the straightforward choice. Use **OnEdge** when you need more natural-feeling movement and only want the mod to step in at the last moment — the sub-settings let you tune exactly how aggressively it reacts and for how long.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Safe | — | Overall behavior: `None` disables protection; `Safe` constantly prevents walking off edges (equivalent to always sneaking at ledges); `OnEdge` only activates when you are close to a drop. |
| Mode → \[OnEdge\] → Distance | Decimal Range | 0.1..0.15 | 0.05..0.5 | How close to a block edge (in blocks) your projected position must be before OnEdge triggers its correction. |
| Mode → \[OnEdge\] → Keep | Integer Range | 1..2 | 1..20 (ticks) | How many ticks the correction stays active after an edge is first detected. A random value in the range is chosen each trigger. |
| Mode → \[OnEdge\] → Mode | Choice | Stop | — | What to do once an edge is detected: `Stop` cancels all movement input; `Invert` reverses your movement direction; `Center` steers you back toward the center of your current block. |
| Mode → \[OnEdge\] → Sneak | Integer Range | 0..0 | 0..20 (ticks) | How many ticks to apply a sneak input after an edge is detected. Set to a non-zero range to add a brief crouch on top of the chosen correction. |
| Mode → \[OnEdge\] → Jump | Toggle | false | — | When enabled, triggers a jump each time the edge correction activates. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleSafeWalk.kt)*
