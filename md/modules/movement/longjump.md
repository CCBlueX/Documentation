## LongJump

Allows you to jump further.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: NoCheatPlusBoost | modes: NoCheatPlusBoost, NoCheatPlusBow, Vulcan289, Matrix-7.14.5-Flag)
│   ├── [Mode: NoCheatPlusBoost]
│   │   └── NCPBoost (Decimal | default: 4.25 | range: 1.0..10.0)
│   ├── [Mode: NoCheatPlusBow]
│   │   ├── Rotations (Setting Group)
│   │   │   ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│   │   │   │   ├── [Mode: Linear]
│   │   │   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │   ├── [Mode: Sigmoid]
│   │   │   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │   │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   │   │   └── [Mode: Acceleration]
│   │   │   │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │   │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │   │       ├── DynamicAccel (Toggleable Group | default: off)
│   │   │   │       │   ├── Enabled (Toggle | default: false)
│   │   │   │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│   │   │   │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │   │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │   │       ├── AccelerationError (Toggleable Group | default: on)
│   │   │   │       │   ├── Enabled (Toggle | default: true)
│   │   │   │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       ├── ConstantError (Toggleable Group | default: on)
│   │   │   │       │   ├── Enabled (Toggle | default: true)
│   │   │   │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       └── SigmoidDeceleration (Toggleable Group | default: off)
│   │   │   │           ├── Enabled (Toggle | default: false)
│   │   │   │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │   │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   │   ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│   │   │   ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│   │   │   └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│   │   ├── Charged (Integer | default: 4 | range: 3..20)
│   │   ├── Speed (Decimal | default: 2.5 | range: 0.0..20.0)
│   │   ├── ArrowsToShoot (Integer | default: 8 | range: 0..20)
│   │   └── FallDistanceToJump (Decimal | default: 0.42 | range: 0.0..2.0)
│   └── [Mode: Matrix-7.14.5-Flag]
│       ├── BoostSpeed (Decimal | default: 1.97 | range: 0.1..5.0)
│       ├── MotionY (Decimal | default: 0.42 | range: 0.0..5.0)
│       └── Delay (Integer | default: 0 | range: 0..3)
├── AutoJump (Toggle | default: false)
└── DisableAfterFinished (Toggle | default: false)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **NoCheatPlusBoost**, **NoCheatPlusBow**, **Vulcan289**, **Matrix-7.14.5-Flag**. Default: **NoCheatPlusBoost**.

##### Mode: NoCheatPlusBoost

- **NCPBoost** (Decimal) — default: `4.25`; range: `1.0` – `10.0` — Horizontal boost multiplier applied on jump for NCP bypass.

##### Mode: NoCheatPlusBow

#### Rotations

> For details on Rotations settings, see [Shared: Rotations](/docs/modules/shared-settings/rotations).

- **Charged** (Integer) — default: `4`; range: `3` – `20` — Number of ticks the bow must be charged before shooting.
- **Speed** (Decimal) — default: `2.5`; range: `0.0` – `20.0` — Horizontal boost speed applied after the bow boost.
- **ArrowsToShoot** (Integer) — default: `8`; range: `0` – `20` — Number of arrows to shoot for boosting.
- **FallDistanceToJump** (Decimal) — default: `0.42`; range: `0.0` – `2.0` — Minimum fall distance before performing the boost jump.

##### Mode: Matrix-7.14.5-Flag

- **BoostSpeed** (Decimal) — default: `1.97`; range: `0.1` – `5.0` — Horizontal boost speed applied during the long jump.
- **MotionY** (Decimal) — default: `0.42`; range: `0.0` – `5.0` — Upward motion applied on jump.
- **Delay** (Integer) — default: `0`; range: `0` – `3` — Ticks to wait before applying the boost.

- **AutoJump** (Toggle) — default: `false` — Automatically jumps when moving on the ground.
- **DisableAfterFinished** (Toggle) — default: `false` — Disables the module after the boosted jump lands.

### Screenshots

*Screenshots for LongJump will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleLongJump.kt)*
