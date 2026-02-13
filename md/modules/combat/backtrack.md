## Backtrack

Causes targets to lag allowing you to attack them more efficiently.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Range (Decimal Range | default: 1.0..3.0 | range: 0.0..10.0)
├── Delay (Integer Range | default: 100..150 | range: 0..1000 | ms)
├── NextBacktrackDelay (Integer Range | default: 0..10 | range: 0..2000 | ms)
├── TrackingBuffer (Integer | default: 500 | range: 0..2000 | ms)
├── Chance (Decimal | default: 50.0 | range: 0.0..100.0 | %)
├── PauseOnHurtTime (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   └── HurtTime (Integer | default: 3 | range: 0..10)
├── TargetMode (Choice | default: ATTACK | options: Attack, Range)
├── LastAttackTimeToWork (Integer | default: 1000 | range: 0..5000)
└── Esp (Mode Selector | default: Wireframe | modes: Box, Model, Wireframe, None)
    ├── [Mode: Box]
    │   ├── Color (Color)
    │   └── Color (Color)
    ├── [Mode: Wireframe]
    │   ├── Color (Color)
    │   └── OutlineColor (Color)
```

### Settings Details

- **Range** (Decimal Range) — default: `1.0` – `3.0`; range: `0.0` – `10.0` — Distance range to the target at which backtracking activates.
- **Delay** (Integer Range) — default: `100` – `150`; range: `0` – `1000`; unit: ms — How long incoming packets are held before being released.
- **NextBacktrackDelay** (Integer Range) — default: `0` – `10`; range: `0` – `2000`; unit: ms — Cooldown before starting a new backtrack after the previous one ends.
- **TrackingBuffer** (Integer) — default: `500`; range: `0` – `2000`; unit: ms — Grace period to keep backtracking after the target leaves the range.
- **Chance** (Decimal) — default: `50.0`; range: `0.0` – `100.0`; unit: % — Probability that backtracking will activate on each encounter.
#### PauseOnHurtTime

A toggleable group of settings (default: disabled). When enabled, pauses backtracking while the target is in their hurt animation.

- **Enabled** (Toggle) — default: `false` — Enables the hurt-time pause check.
- **HurtTime** (Integer) — default: `3`; range: `0` – `10` — Minimum target hurt-time value at which backtracking is paused.

- **TargetMode** (Choice) — default: `ATTACK`; options: `Attack`, `Range` — How targets are selected: Attack uses your last attacked entity; Range finds the nearest enemy.
- **LastAttackTimeToWork** (Integer) — default: `1000`; range: `0` – `5000` — Maximum time in ms since last attack for backtracking to remain active.
#### Esp

Select a mode for this feature. Available modes: **Box**, **Model**, **Wireframe**, **None**. Default: **Wireframe**.

##### Mode: Box

- **Color** (Color) — Fill color of the backtracked entity box.
- **Color** (Color) — Outline color of the backtracked entity box.

##### Mode: Wireframe

- **Color** (Color) — Wireframe color of the backtracked entity.
- **OutlineColor** (Color) — Outline color of the backtracked entity wireframe.


### Screenshots

*Screenshots for Backtrack will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleBacktrack.kt)*
