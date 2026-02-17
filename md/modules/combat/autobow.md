## AutoBow

Automates many bow-related actions like aiming and shooting.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── AutoShoot (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Charged (Integer | default: 15 | range: 3..20 | ticks)
│   ├── ChargedRandom (Decimal Range | default: 0.0..0.0 | range: -10.0..10.0 | ticks)
│   ├── DelayBetweenShots (Decimal | default: 0.0 | range: 0.0..5.0 | s)
│   ├── AimThreshold (Decimal | default: 1.5 | range: 1.0..4.0 | °)
│   ├── RequiresHypotheticalHit (Toggle | default: false)
│   └── UsePrechargedCrossbow (Toggle | default: false)
├── BowAimbot (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Target (Setting Group)
│   │   ├── FOV (Decimal | default: 180.0 | range: 0.0..180.0)
│   │   ├── HurtTime (Integer | default: 10 | range: 0..10)
│   │   └── Priority (Multi-Select | default: [Type, Distance] | options: Type, Health, Distance, Direction, HurtTime, Age)
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
│   └── TargetRendering (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       └── Mode (Mode Selector | default: Image | modes: Legacy, Circle, Image, GlowingCircle, Ghost, Text2D, Arrow)
│           ├── [Mode: Legacy]
│           │   ├── Size (Decimal | default: 0.5 | range: 0.1..2.0)
│           │   ├── Height (Decimal | default: 0.1 | range: 0.02..2.0)
│           │   ├── Color (Color)
│           │   └── ExtraYOffset (Decimal | default: 0.1 | range: 0.0..1.0)
│           ├── [Mode: Circle]
│           │   ├── Radius (Decimal | default: 0.85 | range: 0.1..2.0)
│           │   ├── InnerRadius (Decimal | default: 0.0 | range: 0.0..2.0)
│           │   ├── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
│           │   │   ├── [Mode: Feet]
│           │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│           │   │   ├── [Mode: Top]
│           │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│           │   │   ├── [Mode: Relative]
│           │   │   │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
│           │   │   └── [Mode: Animated]
│           │   │       ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
│           │   │       ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
│           │   │       ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
│           │   │       └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
│           │   ├── OuterColor (Color)
│           │   ├── InnerColor (Color)
│           │   └── Color (Color)
│           ├── [Mode: Image]
│           │   ├── Source (Mode Selector | default: Custom | modes: Custom, Builtin)
│           │   │   ├── [Mode: Custom]
│           │   │   │   └── File (File)
│           │   │   └── [Mode: Builtin]
│           │   │       └── Preset (Choice | default: MARKER1 | options: Marker1, Marker2)
│           │   ├── Scale (2D Position)
│           │   ├── ColorModulator (Color)
│           │   ├── Rotate (Setting Group)
│           │   │   ├── Period (Integer | default: 1000 | range: 10..20000 | ms)
│           │   │   ├── Symmetric (Toggle | default: true)
│           │   │   └── Curve (Curve)
│           │   └── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
│           │       ├── [Mode: Feet]
│           │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│           │       ├── [Mode: Top]
│           │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│           │       ├── [Mode: Relative]
│           │       │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
│           │       └── [Mode: Animated]
│           │           ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
│           │           ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
│           │           ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
│           │           └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
│           ├── [Mode: GlowingCircle]
│           │   ├── Radius (Decimal | default: 0.85 | range: 0.1..2.0)
│           │   ├── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
│           │   │   ├── [Mode: Feet]
│           │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│           │   │   ├── [Mode: Top]
│           │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│           │   │   ├── [Mode: Relative]
│           │   │   │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
│           │   │   └── [Mode: Animated]
│           │   │       ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
│           │   │       ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
│           │   │       ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
│           │   │       └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
│           │   ├── OuterColor (Color)
│           │   ├── GlowColor (Color)
│           │   ├── GlowHeight (Decimal | default: 0.3 | range: -1.0..1.0)
│           │   └── Color (Color)
│           ├── [Mode: Ghost]
│           │   ├── Color (Color)
│           │   ├── Size (Decimal | default: 0.5 | range: 0.4..0.7)
│           │   └── Length (Integer | default: 25 | range: 15..40)
│           ├── [Mode: Text2D]
│           │   ├── Scale (Decimal | default: 1.0 | range: 0.01..10.0)
│           │   ├── Shadow (Toggle | default: true)
│           │   ├── Color (Color)
│           │   ├── Text (Editable List)
│           │   └── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
│           │       ├── [Mode: Feet]
│           │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│           │       ├── [Mode: Top]
│           │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│           │       ├── [Mode: Relative]
│           │       │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
│           │       └── [Mode: Animated]
│           │           ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
│           │           ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
│           │           ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
│           │           └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
│           └── [Mode: Arrow]
│               ├── Color (Color)
│               ├── OutlineColor (Color)
│               └── Size (Decimal | default: 1.5 | range: 0.5..20.0)
└── FastCharge (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── Speed (Integer | default: 20 | range: 3..20)
    ├── NotInTheAir (Toggle | default: true)
    ├── NotDuringMove (Toggle | default: false)
    ├── NotDuringRegeneration (Toggle | default: false)
    └── PacketType (Choice | default: FULL | options: OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full)
```

### Settings Details

#### AutoShoot

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Charged** (Integer) — default: `15`; range: `3` – `20`; unit: ticks — Number of ticks to wait before automatically releasing the bow.
- **ChargedRandom** (Decimal Range) — default: `0.0` – `0.0`; range: `-10.0` – `10.0`; unit: ticks — Random variation added to the charge time using Gaussian distribution.
- **DelayBetweenShots** (Decimal) — default: `0.0`; range: `0.0` – `5.0`; unit: s — Minimum delay in seconds required between consecutive shots.
- **AimThreshold** (Decimal) — default: `1.5`; range: `1.0` – `4.0`; unit: ° — Maximum angle deviation from the target allowed before shooting.
- **RequiresHypotheticalHit** (Toggle) — default: `false` — When enabled, simulates the arrow trajectory to confirm a hit before shooting.
- **UsePrechargedCrossbow** (Toggle) — default: `false` — Enables auto-shooting with pre-charged crossbows in the off-hand.

#### BowAimbot

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### Target

> For details on Target settings, see [Shared: Target](/docs/modules/shared/target).

##### Rotations

> For details on Rotations settings, see [Shared: Rotations](/docs/modules/shared/rotations).

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

##### TargetRendering

> For details on TargetRendering settings, see [Shared: TargetRendering](/docs/modules/shared/target-rendering).

###### Mode: Legacy

- **Size** (Decimal) — default: `0.5`; range: `0.1` – `2.0`
- **Height** (Decimal) — default: `0.1`; range: `0.02` – `2.0`
- **Color** (Color)
- **ExtraYOffset** (Decimal) — default: `0.1`; range: `0.0` – `1.0`

###### Mode: Circle

- **Radius** (Decimal) — default: `0.85`; range: `0.1` – `2.0`
- **InnerRadius** (Decimal) — default: `0.0`; range: `0.0` – `2.0`
###### HeightMode

Select a mode for this feature. Available modes: **Feet**, **Top**, **Relative**, **Health**, **Animated**. Default: **Feet**.

###### Mode: Feet

- **Offset** (Decimal) — default: `0.0`; range: `-1.0` – `1.0`

###### Mode: Top

- **Offset** (Decimal) — default: `0.0`; range: `-1.0` – `1.0`

###### Mode: Relative

- **Height** (Decimal) — default: `0.5`; range: `-0.5` – `1.5`

###### Mode: Animated

- **Speed** (Decimal) — default: `0.18`; range: `0.01` – `1.0`
- **HeightMultiplier** (Decimal) — default: `0.4`; range: `0.1` – `1.0`
- **HeightOffset** (Decimal) — default: `1.3`; range: `0.0` – `2.0`
- **GlowOffset** (Decimal) — default: `-1.0`; range: `-3.1` – `3.1`

- **OuterColor** (Color)
- **InnerColor** (Color)
- **Color** (Color)

###### Mode: Image

###### Source

Select a mode for this feature. Available modes: **Custom**, **Builtin**. Default: **Custom**.

###### Mode: Custom

- **File** (File)

###### Mode: Builtin

- **Preset** (Choice) — default: `MARKER1`; options: `Marker1`, `Marker2`

- **Scale** (2D Position)
- **ColorModulator** (Color)
###### Rotate

A group of related settings.

- **Period** (Integer) — default: `1000`; range: `10` – `20000`; unit: ms
- **Symmetric** (Toggle) — default: `true`
- **Curve** (Curve)

###### HeightMode

Select a mode for this feature. Available modes: **Feet**, **Top**, **Relative**, **Health**, **Animated**. Default: **Feet**.

###### Mode: Feet

- **Offset** (Decimal) — default: `0.0`; range: `-1.0` – `1.0`

###### Mode: Top

- **Offset** (Decimal) — default: `0.0`; range: `-1.0` – `1.0`

###### Mode: Relative

- **Height** (Decimal) — default: `0.5`; range: `-0.5` – `1.5`

###### Mode: Animated

- **Speed** (Decimal) — default: `0.18`; range: `0.01` – `1.0`
- **HeightMultiplier** (Decimal) — default: `0.4`; range: `0.1` – `1.0`
- **HeightOffset** (Decimal) — default: `1.3`; range: `0.0` – `2.0`
- **GlowOffset** (Decimal) — default: `-1.0`; range: `-3.1` – `3.1`


###### Mode: GlowingCircle

- **Radius** (Decimal) — default: `0.85`; range: `0.1` – `2.0`
###### HeightMode

Select a mode for this feature. Available modes: **Feet**, **Top**, **Relative**, **Health**, **Animated**. Default: **Feet**.

###### Mode: Feet

- **Offset** (Decimal) — default: `0.0`; range: `-1.0` – `1.0`

###### Mode: Top

- **Offset** (Decimal) — default: `0.0`; range: `-1.0` – `1.0`

###### Mode: Relative

- **Height** (Decimal) — default: `0.5`; range: `-0.5` – `1.5`

###### Mode: Animated

- **Speed** (Decimal) — default: `0.18`; range: `0.01` – `1.0`
- **HeightMultiplier** (Decimal) — default: `0.4`; range: `0.1` – `1.0`
- **HeightOffset** (Decimal) — default: `1.3`; range: `0.0` – `2.0`
- **GlowOffset** (Decimal) — default: `-1.0`; range: `-3.1` – `3.1`

- **OuterColor** (Color)
- **GlowColor** (Color)
- **GlowHeight** (Decimal) — default: `0.3`; range: `-1.0` – `1.0`
- **Color** (Color)

###### Mode: Ghost

- **Color** (Color)
- **Size** (Decimal) — default: `0.5`; range: `0.4` – `0.7`
- **Length** (Integer) — default: `25`; range: `15` – `40`

###### Mode: Text2D

- **Scale** (Decimal) — default: `1.0`; range: `0.01` – `10.0`
- **Shadow** (Toggle) — default: `true`
- **Color** (Color)
- **Text** (Editable List)
###### HeightMode

Select a mode for this feature. Available modes: **Feet**, **Top**, **Relative**, **Health**, **Animated**. Default: **Feet**.

###### Mode: Feet

- **Offset** (Decimal) — default: `0.0`; range: `-1.0` – `1.0`

###### Mode: Top

- **Offset** (Decimal) — default: `0.0`; range: `-1.0` – `1.0`

###### Mode: Relative

- **Height** (Decimal) — default: `0.5`; range: `-0.5` – `1.5`

###### Mode: Animated

- **Speed** (Decimal) — default: `0.18`; range: `0.01` – `1.0`
- **HeightMultiplier** (Decimal) — default: `0.4`; range: `0.1` – `1.0`
- **HeightOffset** (Decimal) — default: `1.3`; range: `0.0` – `2.0`
- **GlowOffset** (Decimal) — default: `-1.0`; range: `-3.1` – `3.1`


###### Mode: Arrow

- **Color** (Color)
- **OutlineColor** (Color)
- **Size** (Decimal) — default: `1.5`; range: `0.5` – `20.0`



#### FastCharge

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Speed** (Integer) — default: `20`; range: `3` – `20` — Number of movement packets sent per tick to accelerate bow charging.
- **NotInTheAir** (Toggle) — default: `true` — Disables fast charging when the player is airborne.
- **NotDuringMove** (Toggle) — default: `false` — Disables fast charging while the player is moving.
- **NotDuringRegeneration** (Toggle) — default: `false` — Disables fast charging while the regeneration effect is active.
- **PacketType** (Choice) — default: `FULL`; options: `OnGroundOnly`, `PositionAndOnGround`, `LookAndOnGround`, `Full` — Type of movement packet sent to accelerate bow charge.


### Screenshots

*Screenshots for AutoBow will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleAutoBow.kt)*
