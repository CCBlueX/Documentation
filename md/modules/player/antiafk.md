## AntiAFK

Prevents you from being kicked for being AFK.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: RandomInteraction | modes: Old, RandomInteraction, Custom)
    ├── [Mode: RandomInteraction]
    │   ├── Interaction (Multi-Select | default: [SwingHand, Yaw, Pitch] | options: Jump, SwingHand, ChangeSlot, Yaw, Pitch, RandomDirection)
    │   └── Delay (Integer Range | default: 4..7 | range: 0..20 | ticks)
    └── [Mode: Custom]
        ├── Rotate (Toggleable Group | default: on)
        │   ├── Enabled (Toggle | default: true)
        │   ├── IgnoreOpenInventory (Toggle | default: true)
        │   ├── Rotations (Setting Group)
        │   │   ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
        │   │   │   ├── [Mode: Linear]
        │   │   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
        │   │   │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
        │   │   │   ├── [Mode: Sigmoid]
        │   │   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
        │   │   │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
        │   │   │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
        │   │   │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
        │   │   │   └── [Mode: Acceleration]
        │   │   │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
        │   │   │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
        │   │   │       ├── DynamicAccel (Toggleable Group | default: off)
        │   │   │       │   ├── Enabled (Toggle | default: false)
        │   │   │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
        │   │   │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
        │   │   │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
        │   │   │       ├── AccelerationError (Toggleable Group | default: on)
        │   │   │       │   ├── Enabled (Toggle | default: true)
        │   │   │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
        │   │   │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
        │   │   │       ├── ConstantError (Toggleable Group | default: on)
        │   │   │       │   ├── Enabled (Toggle | default: true)
        │   │   │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
        │   │   │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
        │   │   │       └── SigmoidDeceleration (Toggleable Group | default: off)
        │   │   │           ├── Enabled (Toggle | default: false)
        │   │   │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
        │   │   │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
        │   │   ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
        │   │   ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
        │   │   └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
        │   ├── Delay (Integer | default: 5 | range: 0..20 | ticks)
        │   └── Angle (Decimal | default: 1.0 | range: -180.0..180.0)
        ├── Swing (Toggleable Group | default: on)
        │   ├── Enabled (Toggle | default: true)
        │   └── Delay (Integer | default: 5 | range: 0..20 | ticks)
        ├── Jump (Toggle | default: true)
        └── Move (Toggle | default: true)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Old**, **RandomInteraction**, **Custom**. Default: **RandomInteraction**.

##### Mode: RandomInteraction

- **Interaction** (Multi-Select) — default: `SwingHand`, `Yaw`, `Pitch`; options: `Jump`, `SwingHand`, `ChangeSlot`, `Yaw`, `Pitch`, `RandomDirection` — Types of random interactions to perform.
- **Delay** (Integer Range) — default: `4` – `7`; range: `0` – `20`; unit: ticks — Ticks to wait between each random interaction.

##### Mode: Custom

###### Rotate

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **IgnoreOpenInventory** (Toggle) — default: `true` — Rotates even when the inventory screen is open.
###### Rotations

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

- **Delay** (Integer) — default: `5`; range: `0` – `20`; unit: ticks — Ticks to wait between each rotation.
- **Angle** (Decimal) — default: `1.0`; range: `-180.0` – `180.0` — Yaw angle added to each rotation.

###### Swing

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Delay** (Integer) — default: `5`; range: `0` – `20`; unit: ticks — Ticks to wait between each hand swing.

- **Jump** (Toggle) — default: `true` — Periodically jumps while enabled.
- **Move** (Toggle) — default: `true` — Automatically walks forward while enabled.


### Screenshots

*Screenshots for AntiAFK will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleAntiAFK.kt)*
