## EasyPearl

Throws pearl to where you looking at.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── AimOffThreshold (Decimal | default: 2.0 | range: 0.5..10.0)
├── ReachableCheck (Toggle | default: true)
└── Rotations (Setting Group)
    ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
    │   ├── [Mode: Linear]
    │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
    │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
    │   ├── [Mode: Sigmoid]
    │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
    │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
    │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
    │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
    │   └── [Mode: Acceleration]
    │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
    │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
    │       ├── DynamicAccel (Toggleable Group | default: off)
    │       │   ├── Enabled (Toggle | default: false)
    │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
    │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
    │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
    │       ├── AccelerationError (Toggleable Group | default: on)
    │       │   ├── Enabled (Toggle | default: true)
    │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
    │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
    │       ├── ConstantError (Toggleable Group | default: on)
    │       │   ├── Enabled (Toggle | default: true)
    │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
    │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
    │       └── SigmoidDeceleration (Toggleable Group | default: off)
    │           ├── Enabled (Toggle | default: false)
    │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
    │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
    ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
    ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
    └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
```

### Settings Details

- **AimOffThreshold** (Decimal) — default: `2.0`; range: `0.5` – `10.0`
- **ReachableCheck** (Toggle) — default: `true`
#### Rotations

A group of related settings.

##### AngleSmooth

Select a mode for this feature. Available modes: **Linear**, **Sigmoid**, **Acceleration**. Default: **Linear**.

###### Mode: Linear

- **HorizontalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **VerticalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`

###### Mode: Sigmoid

- **HorizontalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **VerticalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **Steepness** (Decimal) — default: `10.0`; range: `0.0` – `20.0`
- **Midpoint** (Decimal) — default: `0.3`; range: `0.0` – `1.0`

###### Mode: Acceleration

- **YawAcceleration** (Decimal Range) — default: `20.0` – `25.0`; range: `1.0` – `180.0`
- **PitchAcceleration** (Decimal Range) — default: `20.0` – `25.0`; range: `1.0` – `180.0`
###### DynamicAccel

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **CoefDistance** (Decimal) — default: `-1.393`; range: `-2.0` – `2.0`
- **YawCrosshairAccel** (Decimal Range) — default: `17.0` – `20.0`; range: `1.0` – `180.0`
- **PitchCrosshairAccel** (Decimal Range) — default: `17.0` – `20.0`; range: `1.0` – `180.0`

###### AccelerationError

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **YawAccelError** (Decimal) — default: `0.1`; range: `0.01` – `1.0`
- **PitchAccelError** (Decimal) — default: `0.1`; range: `0.01` – `1.0`

###### ConstantError

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **YawConstantError** (Decimal) — default: `0.1`; range: `0.01` – `1.0`
- **PitchConstantError** (Decimal) — default: `0.1`; range: `0.01` – `1.0`

###### SigmoidDeceleration

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Steepness** (Decimal) — default: `10.0`; range: `0.0` – `20.0`
- **Midpoint** (Decimal) — default: `0.3`; range: `0.0` – `1.0`


- **MovementCorrection** (Choice) — default: `SILENT`; options: `Off`, `Strict`, `Silent`, `ChangeLook`
- **ResetThreshold** (Decimal) — default: `2.0`; range: `1.0` – `180.0`
- **TicksUntilReset** (Integer) — default: `5`; range: `1` – `30`; unit: ticks


### Screenshots

*Screenshots for EasyPearl will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleEasyPearl.kt)*
