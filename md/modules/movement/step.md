## Step

Allows you to step up blocks faster.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: Instant | modes: Instant, Legit, Vulcan286, BlocksMC, Hypixel)
    ├── [Mode: Instant]
    │   ├── Height (Decimal | default: 1.0 | range: 0.6..5.0)
    │   ├── Trim (Toggle | default: false)
    │   ├── SimulateJumpOrder (Integer Range | default: 0..2 | range: 0..8)
    │   ├── Wait (Integer Range | default: 0..0 | range: 0..60 | ticks)
    │   └── PacketType (Choice | default: FULL | options: PositionAndOnGround, Full)
    ├── [Mode: BlocksMC]
    │   ├── BaseTimer (Decimal | default: 3.0 | range: 0.1..5.0)
    │   └── RecoveryTimer (Decimal | default: 0.6 | range: 0.1..5.0)
    └── [Mode: Hypixel]
        ├── AlternateBypass (Toggle | default: false)
        └── Spoof (Toggle | default: false)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Instant**, **Legit**, **Vulcan286**, **BlocksMC**, **Hypixel**. Default: **Instant**.

##### Mode: Instant

- **Height** (Decimal) — default: `1.0`; range: `0.6` – `5.0` — Maximum step-up height allowed.
- **Trim** (Toggle) — default: `false` — Trims simulated jump packets to not exceed the actual step height.
- **SimulateJumpOrder** (Integer Range) — default: `0` – `2`; range: `0` – `8` — Range of jump simulation packets to send for anti-cheat bypass.
- **Wait** (Integer Range) — default: `0` – `0`; range: `0` – `60`; unit: ticks — Number of ticks to wait between steps.
- **PacketType** (Choice) — default: `FULL`; options: `PositionAndOnGround`, `Full` — Type of movement packet to send during step simulation.

##### Mode: BlocksMC

- **BaseTimer** (Decimal) — default: `3.0`; range: `0.1` – `5.0` — Timer speed multiplier during the step.
- **RecoveryTimer** (Decimal) — default: `0.6`; range: `0.1` – `5.0` — Timer speed multiplier for recovery after stepping.

##### Mode: Hypixel

- **AlternateBypass** (Toggle) — default: `false` — Uses an alternate ground-spoof method for stepping on Hypixel.
- **Spoof** (Toggle) — default: `false` — Spoofs ground state at a specific air tick to bypass checks.


### Screenshots

*Screenshots for Step will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2Fstep%2FModuleStep.kt)*
