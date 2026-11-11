## SafeWalk

SafeWalk stops you from walking off the edge of a block, like holding Sneak but without slowing down. Turn it on when you build or walk on narrow bridges high up.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Safe | None, Safe, OnEdge | None: no protection. Safe: you can never walk off an edge. OnEdge: steps in only when you are about to fall off. |
| Mode → OnEdge → Distance | Decimal Range | 0.1..0.15 | 0.05..0.5 | How close to the edge (in blocks) you can get before it steps in. |
| Mode → OnEdge → Keep | Integer Range | 1..2 | 1..20 ticks | How long it keeps holding you back, in ticks (20 per second). |
| Mode → OnEdge → Mode | Choice | Stop | Stop, Invert, Center | What happens at the edge. Stop: you stop. Invert: you walk the other way. Center: you walk back to the middle of your block. |
| Mode → OnEdge → Sneak | Integer Range | 0..0 | 0..20 ticks | How long you also sneak at the edge. 0 means never. |
| Mode → OnEdge → Jump | Toggle | false |  | Jumps every time it stops you at an edge. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleSafeWalk.kt)*
