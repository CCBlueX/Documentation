## FastExp

Automatically repairs your armor.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
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
├── NoWaste (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── MinDurabilityToStartRepair (Integer | default: 64 | range: 0..2048)
│   └── MaxDurabilityToContinueRepair (Integer | default: 85 | range: 1..100 | %)
├── ThrowMode (Mode Selector | default: Normal | modes: Normal, Fast)
│   ├── [Mode: Normal]
│   │   └── TicksPerItem (Decimal Range | default: 2.0..3.0 | range: 0.5..10.0 | ticks)
│   └── [Mode: Fast]
│       └── ItemsPerTick (Decimal Range | default: 3.0..5.0 | range: 0.5..16.0)
├── CombatPauseTime (Integer | default: 0 | range: 0..40 | ticks)
└── SlotResetDelay (Integer Range | default: 0..0 | range: 0..40 | ticks)
```

### Settings Details

#### Rotate

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### Rotations

A group of related settings. *Shared setting group — configured identically across modules that use rotations.*

###### AngleSmooth

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


#### NoWaste

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **MinDurabilityToStartRepair** (Integer) — default: `64`; range: `0` – `2048` — Durability threshold below which the module starts throwing experience bottles.
- **MaxDurabilityToContinueRepair** (Integer) — default: `85`; range: `1` – `100`; unit: % — Maximum durability percentage at which repair continues after an interruption.

#### ThrowMode

Select a mode for this feature. Available modes: **Normal**, **Fast**. Default: **Normal**.

##### Mode: Normal

- **TicksPerItem** (Decimal Range) — default: `2.0` – `3.0`; range: `0.5` – `10.0`; unit: ticks — Ticks to wait between each experience bottle throw.

##### Mode: Fast

- **ItemsPerTick** (Decimal Range) — default: `3.0` – `5.0`; range: `0.5` – `16.0` — Number of experience bottles thrown per tick.

- **CombatPauseTime** (Integer) — default: `0`; range: `0` – `40`; unit: ticks — Ticks to pause combat actions before throwing bottles.
- **SlotResetDelay** (Integer Range) — default: `0` – `0`; range: `0` – `40`; unit: ticks — Ticks to wait before switching back to the original hotbar slot.

### Screenshots

*Screenshots for FastExp will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleFastExp.kt)*
