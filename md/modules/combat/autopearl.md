## AutoPearl

Aims and throws a pearl at an enemies pearl trajectory.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Choice | default: TRIGGER | options: Trigger, Target)
├── Rotate (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Rotations (Setting Group)
│       ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│       │   ├── [Mode: Linear]
│       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   ├── [Mode: Sigmoid]
│       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│       │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│       │   └── [Mode: Acceleration]
│       │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│       │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│       │       ├── DynamicAccel (Toggleable Group | default: off)
│       │       │   ├── Enabled (Toggle | default: false)
│       │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│       │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│       │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│       │       ├── AccelerationError (Toggleable Group | default: on)
│       │       │   ├── Enabled (Toggle | default: true)
│       │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       ├── ConstantError (Toggleable Group | default: on)
│       │       │   ├── Enabled (Toggle | default: true)
│       │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       └── SigmoidDeceleration (Toggleable Group | default: off)
│       │           ├── Enabled (Toggle | default: false)
│       │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│       │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│       ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│       ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│       └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
├── Limits (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Angle (Integer | default: 180 | range: 0..180 | °)
│   ├── MinDistance (Decimal | default: 8.0 | range: 0.0..10.0 | m)
│   └── DestinationDistance (Decimal | default: 8.0 | range: 0.0..30.0 | m)
├── CombatPauseTime (Integer | default: 0 | range: 0..40 | ticks)
└── SlotResetDelay (Integer Range | default: 0..0 | range: 0..40 | ticks)
```

### Settings Details

- **Mode** (Choice) — default: `TRIGGER`; options: `Trigger`, `Target` — Trigger responds to any hostile pearl; Target only responds to the current KillAura target's pearl.
#### Rotate

A toggleable group of settings (default: enabled). When enabled, rotates your view to aim the pearl throw.

- **Enabled** (Toggle) — default: `true` — Enables server-side rotation for aiming.
##### Rotations

> For details on Rotations settings, see [Shared: Rotations](/docs/modules/shared/rotations).


#### Limits

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables the Limits group.
- **Angle** (Integer) — default: `180`; range: `0` – `180`; unit: ° — Maximum crosshair angle to the enemy pearl for the module to trigger.
- **MinDistance** (Decimal) — default: `8.0`; range: `0.0` – `10.0`; unit: m — Minimum distance to the pearl destination required to throw.
- **DestinationDistance** (Decimal) — default: `8.0`; range: `0.0` – `30.0`; unit: m — Maximum allowed distance between your pearl's landing and the enemy pearl's landing.

- **CombatPauseTime** (Integer) — default: `0`; range: `0` – `40`; unit: ticks — Duration to pause combat actions while throwing the pearl.
- **SlotResetDelay** (Integer Range) — default: `0` – `0`; range: `0` – `40`; unit: ticks — Delay before switching back to the previous hotbar slot after throwing.

### Screenshots

*Screenshots for AutoPearl will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleAutoPearl.kt)*
