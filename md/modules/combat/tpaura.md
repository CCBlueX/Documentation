## TpAura

Automatically teleports and attacks enemies around you.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── AttackRange (Decimal | default: 4.2 | range: 3.0..5.0)
├── Clicker (Setting Group)
│   ├── CPS (Integer Range | default: 5..8 | range: 1..60 | clicks)
│   ├── Technique (Choice | default: STABILIZED | options: Stabilized, Efficient, Spamming, DoubleClick, Drag, Butterfly, NormalDistribution)
│   ├── ItemCooldown (Setting Group)
│   │   └── Minimum (Decimal Range | default: 1.0..1.0 | range: 0.0..2.0)
│   └── AttackCooldown (Toggle | default: true)
├── Mode (Mode Selector | default: AStar | modes: AStar, Immediate)
│   ├── [Mode: AStar]
│   │   ├── MaximumDistance (Integer | default: 95 | range: 50..250)
│   │   ├── MaximumCost (Integer | default: 250 | range: 50..500)
│   │   ├── TickDistance (Integer | default: 3 | range: 1..7)
│   │   ├── AllowDiagonal (Toggle | default: false)
│   │   ├── TpBack (Toggle | default: true)
│   │   └── Stick (Integer | default: 5 | range: 1..10 | ticks)
└── Target (Setting Group)
    ├── FOV (Decimal | default: 180.0 | range: 0.0..180.0)
    ├── HurtTime (Integer | default: 10 | range: 0..10)
    └── Priority (Multi-Select | default: [Type, HurtTime] | options: Type, Health, Distance, Direction, HurtTime, Age)
```

### Settings Details

- **AttackRange** (Decimal) — default: `4.2`; range: `3.0` – `5.0` — Maximum distance from the desync position at which enemies can be attacked.
#### Clicker

> For details on Clicker settings, see [Shared: Clicker](/docs/modules/shared/clicker).

#### Mode

Select a mode for this feature. Available modes: **AStar**, **Immediate**. Default: **AStar**.

##### Mode: AStar

- **MaximumDistance** (Integer) — default: `95`; range: `50` – `250` — Maximum pathfinding distance in blocks to search for a route to the target.
- **MaximumCost** (Integer) — default: `250`; range: `50` – `500` — Maximum A* path cost before the search is abandoned.
- **TickDistance** (Integer) — default: `3`; range: `1` – `7` — Number of path nodes to traverse per teleport packet.
- **AllowDiagonal** (Toggle) — default: `false` — Allows diagonal movement in the A* pathfinding.
- **TpBack** (Toggle) — default: `true` — Teleports back to the original position after attacking.
- **Stick** (Integer) — default: `5`; range: `1` – `10`; unit: ticks — Ticks to remain at the target position before teleporting back.

#### Target

> For details on Target settings, see [Shared: Target](/docs/modules/shared/target).


### Screenshots

*Screenshots for TpAura will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleTPAura.kt)*
