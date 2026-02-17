## FreeCam

Allows you to move the camera out of your body.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Speed (Decimal | default: 1.0 | range: 0.1..2.0)
├── CancelOn (Multi-Select | options: Damage, Move, Liquid)
├── MidClickCameraTeleport (Toggle | default: false)
├── KeepSneaking (Toggle | default: false)
├── Rotations (Setting Group)
│   ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│   │   ├── [Mode: Linear]
│   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   ├── [Mode: Sigmoid]
│   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   └── [Mode: Acceleration]
│   │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │       ├── DynamicAccel (Toggleable Group | default: off)
│   │       │   ├── Enabled (Toggle | default: false)
│   │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│   │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │       ├── AccelerationError (Toggleable Group | default: on)
│   │       │   ├── Enabled (Toggle | default: true)
│   │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       ├── ConstantError (Toggleable Group | default: on)
│   │       │   ├── Enabled (Toggle | default: true)
│   │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       └── SigmoidDeceleration (Toggleable Group | default: off)
│   │           ├── Enabled (Toggle | default: false)
│   │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│   ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│   └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
├── AllowCameraInteract (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── LookAt (Toggle | default: true)
└── Navigation (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── Auto (Multi-Select | default: [Jump, Swim, Sprint] | options: Jump, Swim, Sprint)
    └── Key (Key)
```

### Settings Details

- **Speed** (Decimal) — default: `1.0`; range: `0.1` – `2.0` — Movement speed of the free camera.
- **CancelOn** (Multi-Select) — options: `Damage`, `Move`, `Liquid` — Events that automatically disable FreeCam.
- **MidClickCameraTeleport** (Toggle) — default: `false` — Teleports the camera to the crosshair target on middle click.
- **KeepSneaking** (Toggle) — default: `false` — Keeps the player sneaking while in FreeCam.
#### Rotations

A group of related settings.

##### AngleSmooth

Select a mode for this feature. Available modes: **Linear**, **Sigmoid**, **Acceleration**. Default: **Linear**.

###### Mode: Linear

- **HorizontalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0` — Horizontal rotation speed range.
- **VerticalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0` — Vertical rotation speed range.

###### Mode: Sigmoid

- **HorizontalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0` — Horizontal rotation speed range.
- **VerticalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0` — Vertical rotation speed range.
- **Steepness** (Decimal) — default: `10.0`; range: `0.0` – `20.0` — Controls how sharply the sigmoid curve transitions.
- **Midpoint** (Decimal) — default: `0.3`; range: `0.0` – `1.0` — The rotation fraction where the sigmoid curve is centered.

###### Mode: Acceleration

- **YawAcceleration** (Decimal Range) — default: `20.0` – `25.0`; range: `1.0` – `180.0` — Yaw acceleration speed range.
- **PitchAcceleration** (Decimal Range) — default: `20.0` – `25.0`; range: `1.0` – `180.0` — Pitch acceleration speed range.
###### DynamicAccel

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles dynamic acceleration based on crosshair distance.
- **CoefDistance** (Decimal) — default: `-1.393`; range: `-2.0` – `2.0` — Distance coefficient for dynamic acceleration scaling.
- **YawCrosshairAccel** (Decimal Range) — default: `17.0` – `20.0`; range: `1.0` – `180.0` — Yaw acceleration when near the crosshair target.
- **PitchCrosshairAccel** (Decimal Range) — default: `17.0` – `20.0`; range: `1.0` – `180.0` — Pitch acceleration when near the crosshair target.

###### AccelerationError

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles random acceleration error for realism.
- **YawAccelError** (Decimal) — default: `0.1`; range: `0.01` – `1.0` — Random error applied to yaw acceleration.
- **PitchAccelError** (Decimal) — default: `0.1`; range: `0.01` – `1.0` — Random error applied to pitch acceleration.

###### ConstantError

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles a constant random rotation error.
- **YawConstantError** (Decimal) — default: `0.1`; range: `0.01` – `1.0` — Constant random error applied to yaw.
- **PitchConstantError** (Decimal) — default: `0.1`; range: `0.01` – `1.0` — Constant random error applied to pitch.

###### SigmoidDeceleration

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles sigmoid-based deceleration near the target.
- **Steepness** (Decimal) — default: `10.0`; range: `0.0` – `20.0` — Controls how sharply the sigmoid deceleration transitions.
- **Midpoint** (Decimal) — default: `0.3`; range: `0.0` – `1.0` — The rotation fraction where the sigmoid deceleration is centered.


- **MovementCorrection** (Choice) — default: `SILENT`; options: `Off`, `Strict`, `Silent`, `ChangeLook` — Corrects movement direction relative to server-side rotation.
- **ResetThreshold** (Decimal) — default: `2.0`; range: `1.0` – `180.0` — Angle difference required to trigger a rotation reset.
- **TicksUntilReset** (Integer) — default: `5`; range: `1` – `30`; unit: ticks — Ticks of inactivity before rotation resets to player direction.

#### AllowCameraInteract

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles interaction from the camera's perspective.
- **LookAt** (Toggle) — default: `true` — Aims at the crosshair target from the camera position.

#### Navigation

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles pathfinding navigation for FreeCam.
- **Auto** (Multi-Select) — default: `Jump`, `Swim`, `Sprint`; options: `Jump`, `Swim`, `Sprint` — Automatic movement actions while navigating.
- **Key** (Key) — Key to hold to navigate toward the camera look target.


### Screenshots

*Screenshots for FreeCam will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleFreeCam.kt)*
