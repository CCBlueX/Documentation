## TargetStrafe

Automatically strafes around enemies targeted by KillAura.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Motion | modes: Motion)
│   └── [Mode: Motion]
│       ├── ControlDirection (Toggle | default: true)
│       ├── Hypixel (Toggle | default: false)
│       ├── Validation (Toggleable Group | default: on)
│       │   ├── Enabled (Toggle | default: true)
│       │   ├── EdgeCheck (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   └── MaxFallHeight (Decimal | default: 1.2 | range: 0.1..4.0)
│       │   └── VoidCheck (Toggleable Group | default: on)
│       │       ├── Enabled (Toggle | default: true)
│       │       └── SafetyExpand (Decimal | default: 0.1 | range: 0.0..5.0)
│       └── AdaptiveRange (Toggleable Group | default: off)
│           ├── Enabled (Toggle | default: false)
│           ├── MaxRange (Decimal | default: 4.0 | range: 1.0..5.0)
│           └── RangeStep (Decimal | default: 0.5 | range: 0.0..1.0)
├── Range (Decimal | default: 2.95 | range: 0.0..8.0)
├── FollowRange (Decimal | default: 4.0 | range: 0.0..10.0)
└── Requirements (Multi-Select | options: Space, Speed, KillAura, Ground)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Motion**. Default: **Motion**.

##### Mode: Motion

- **ControlDirection** (Toggle) — default: `true` — Allows left/right keys to control strafe direction.
- **Hypixel** (Toggle) — default: `false` — Applies Hypixel-specific speed adjustments during strafing.
###### Validation

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles safety validation for strafe positions.
###### EdgeCheck

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables edge detection to prevent falling off ledges.
- **MaxFallHeight** (Decimal) — default: `1.2`; range: `0.1` – `4.0` — Maximum fall height before a position is considered unsafe.

###### VoidCheck

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables void detection to prevent falling into the void.
- **SafetyExpand** (Decimal) — default: `0.1`; range: `0.0` – `5.0` — Expand radius for the void safety check.


###### AdaptiveRange

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Enables dynamic range adjustment when the path is blocked.
- **MaxRange** (Decimal) — default: `4.0`; range: `1.0` – `5.0` — Maximum strafe range when adapting.
- **RangeStep** (Decimal) — default: `0.5`; range: `0.0` – `1.0` — Increment step for range adaptation attempts.


- **Range** (Decimal) — default: `2.95`; range: `0.0` – `8.0` — Maximum distance to consider entities as strafe targets.
- **FollowRange** (Decimal) — default: `4.0`; range: `0.0` – `10.0` — Maximum distance to follow and strafe around a target.
- **Requirements** (Multi-Select) — options: `Space`, `Speed`, `KillAura`, `Ground` — Conditions that must be met for strafing to activate.

### Screenshots

*Screenshots for TargetStrafe will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleTargetStrafe.kt)*
