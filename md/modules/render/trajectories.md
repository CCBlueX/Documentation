## Trajectories

Allows you to see where projectiles will land.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── MaxSimulatedTicks (Integer | default: 240 | range: 1..1000 | ticks)
├── Show (Multi-Select | default: [OtherPlayers, ActiveTrajectoryArrow] | options: AlwaysShowBow, OtherPlayers, ActiveTrajectoryArrow, ActiveTrajectoryOther)
└── ShowDetailedInfo (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── ShowAt (Choice | default: ENTITY | options: Owner, Entity, Landing)
    ├── Item (Toggle | default: true)
    ├── OwnerName (Toggle | default: true)
    ├── Distance (Toggle | default: true)
    ├── DurationUnit (Choice | default: TICKS | options: Ticks, Seconds)
    ├── Color (Color)
    ├── Scale (Decimal | default: 1.0 | range: 0.25..4.0)
    └── RenderOffset (3D Position)
```

### Settings Details

- **MaxSimulatedTicks** (Integer) — default: `240`; range: `1` – `1000`; unit: ticks — Limits the maximum number of ticks to simulate for trajectory prediction.
- **Show** (Multi-Select) — default: `OtherPlayers`, `ActiveTrajectoryArrow`; options: `AlwaysShowBow`, `OtherPlayers`, `ActiveTrajectoryArrow`, `ActiveTrajectoryOther` — Selects which trajectory types to display.
#### ShowDetailedInfo

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Enables the detailed info overlay for trajectories.
- **ShowAt** (Choice) — default: `ENTITY`; options: `Owner`, `Entity`, `Landing` — Selects where to render the detailed info label.
- **Item** (Toggle) — default: `true` — Shows the projectile item icon in the info label.
- **OwnerName** (Toggle) — default: `true` — Shows the name of the entity that launched the projectile.
- **Distance** (Toggle) — default: `true` — Shows the distance to the landing point.
- **DurationUnit** (Choice) — default: `TICKS`; options: `Ticks`, `Seconds` — Selects the time unit for flight duration display.
- **Color** (Color) — Sets the color of the info label text.
- **Scale** (Decimal) — default: `1.0`; range: `0.25` – `4.0` — Sets the scale of the info label.
- **RenderOffset** (3D Position) — Offsets the info label render position.


### Screenshots

*Screenshots for Trajectories will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2Ftrajectories%2FModuleTrajectories.kt)*
