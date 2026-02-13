## Scaffold

Automatically places blocks beneath your feet allowing you to walk across gaps.

**Category:** World  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Delay (Integer Range | default: 0..0 | range: 0..40 | ticks)
├── MinDist (Decimal | default: 0.0 | range: 0.0..0.25)
├── Timer (Decimal | default: 1.0 | range: 0.01..10.0)
├── BlockItemSelection (Setting Group)
│   ├── Disallowed (Registry List)
│   └── Unfavorable (Registry List)
├── AutoBlock (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Always (Toggle | default: false)
│   ├── SlotResetDelay (Integer | default: 5 | range: 0..40 | ticks)
│   └── DoNotUseBelowCount (Integer | default: 1 | range: 0..64)
├── Prediction (Toggleable Group | default: on)
│   └── Enabled (Toggle | default: true)
├── Technique (Mode Selector | default: Normal | modes: Normal, Expand, GodBridge, Breezily)
│   ├── [Mode: Normal]
│   │   ├── RotationMode (Choice | default: STABILIZED | options: Center, Random, Stabilized, NearestRotation, ReverseYaw, DiagonalYaw, AngleYaw, EdgePoint)
│   │   ├── RequiresSight (Toggle | default: false)
│   │   ├── Eagle (Toggleable Group | default: off)
│   │   │   ├── Enabled (Toggle | default: false)
│   │   │   ├── BlocksToEagle (Integer Range | default: 0..0 | range: 0..10)
│   │   │   ├── EdgeDistance (Decimal | default: 0.01 | range: 0.01..1.3)
│   │   │   └── OnlyOnGround (Toggle | default: true)
│   │   ├── Telly (Toggleable Group | default: off)
│   │   │   ├── Enabled (Toggle | default: false)
│   │   │   ├── ResetMode (Choice | default: RESET | options: Reverse, Reset)
│   │   │   ├── Straight (Integer | default: 0 | range: 0..5 | ticks)
│   │   │   ├── Jump (Integer Range | default: 0..0 | range: 0..10 | ticks)
│   │   │   └── AimOnTower (Toggle | default: true)
│   │   ├── Down (Toggleable Group | default: off)
│   │   │   └── Enabled (Toggle | default: false)
│   │   ├── StabilizeMovement (Toggleable Group | default: on)
│   │   │   └── Enabled (Toggle | default: true)
│   │   ├── Ceiling (Toggleable Group | default: off)
│   │   │   └── Enabled (Toggle | default: false)
│   │   └── HeadHitter (Toggleable Group | default: off)
│   │       └── Enabled (Toggle | default: false)
│   ├── [Mode: Expand]
│   │   └── Length (Integer | default: 4 | range: 1..10 | blocks)
│   ├── [Mode: GodBridge]
│   │   ├── Modes (Multi-Select | default: [Jump] | options: Jump, Sneak, StopInput, Backwards)
│   │   ├── ForceSneakBelowCount (Integer | default: 3 | range: 0..10)
│   │   └── SneakTime (Integer Range | default: 1..1 | range: 1..10)
│   └── [Mode: Breezily]
│       └── EdgeDistance (Decimal Range | default: 0.45..0.5 | range: 0.25..0.5 | blocks)
├── SameY (Choice | default: OFF | options: Off, On, Falling, Hypixel)
├── Tower (Mode Selector | default: None | modes: None, Motion, Pulldown, Karhu, Vulcan, Hypixel)
│   ├── [Mode: Motion]
│   │   ├── Motion (Decimal | default: 0.42 | range: 0.0..1.0)
│   │   ├── TriggerHeight (Decimal | default: 0.78 | range: 0.76..1.0)
│   │   └── Slow (Decimal | default: 1.0 | range: 0.0..3.0)
│   ├── [Mode: Pulldown]
│   │   └── Trigger (Decimal | default: 0.1 | range: 0.0..0.2 | Y/v)
│   ├── [Mode: Karhu]
│   │   ├── Timer (Decimal | default: 5.0 | range: 0.1..10.0)
│   │   ├── Trigger (Decimal | default: 0.06 | range: 0.0..0.2 | Y/v)
│   │   └── Pulldown (Toggle | default: true)
├── SafeWalk (Mode Selector | default: Safe | modes: None, Safe, OnEdge)
│   └── [Mode: OnEdge]
│       ├── Distance (Decimal | default: 0.1 | range: 0.1..0.5)
│       ├── Keep (Integer Range | default: 1..2 | range: 1..20 | ticks)
│       ├── Mode (Choice | default: STOP | options: Stop, Invert, Center)
│       ├── Sneak (Integer Range | default: 0..0 | range: 0..20 | ticks)
│       └── Jump (Toggle | default: false)
├── Swing (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
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
│   ├── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│   ├── ConsiderInventory (Toggle | default: false)
│   └── RotationTiming (Choice | default: NORMAL | options: Normal, OnTick, OnTickSnap)
├── SprintControl (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── Client (Choice | default: DO_NOT_CHANGE | options: DoNotChange, ForceSprint, ForceNoSprint, NoSprintOnPlace, NoSprintOnGround)
│   └── Server (Choice | default: DO_NOT_CHANGE | options: DoNotChange, ForceSprint, ForceNoSprint, NoSprintOnPlace, NoSprintOnGround)
├── SimulatePlacementAttempts (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── Clicker (Setting Group)
│   │   ├── CPS (Integer Range | default: 5..8 | range: 1..100 | clicks)
│   │   └── Technique (Choice | default: STABILIZED | options: Stabilized, Efficient, Spamming, DoubleClick, Drag, Butterfly, NormalDistribution)
│   └── FailedAttemptsOnly (Toggle | default: true)
├── Acceleration (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── SpeedMultiplier (Decimal | default: 0.6 | range: 0.1..3.0)
│   └── OnlyOnGround (Toggle | default: false)
├── Strafe (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── Speed (Decimal | default: 0.247 | range: 0.0..5.0)
│   ├── Hypixel (Toggle | default: false)
│   └── OnlyOnGround (Toggle | default: false)
├── StrafeOnJump (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── StraightSpeed (Decimal Range | default: 0.48..0.49 | range: 0.1..1.0)
│   └── DiagonalSpeed (Decimal Range | default: 0.48..0.49 | range: 0.1..1.0)
├── SpeedLimiter (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   └── SpeedLimit (Decimal | default: 0.11 | range: 0.01..0.4)
├── Blink (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── Time (Integer Range | default: 50..250 | range: 0..3000 | ms)
│   └── FlushOn (Multi-Select | options: Place, Towering, Sneaking, NotSneaking, OnGround, InAir)
├── AutoSpeed (Toggle | default: false)
├── Ledge (Toggle | default: true)
└── Render (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── Clump (Toggle | default: true)
    ├── StartSize (Decimal | default: 1.0 | range: 0.0..2.0)
    ├── StartCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── EndSize (Decimal | default: 0.8 | range: 0.0..2.0)
    ├── EndCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── FadeInCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── FadeOutCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── InTime (Integer | default: 500 | range: 0..5000 | ms)
    ├── OutTime (Integer | default: 500 | range: 0..5000 | ms)
    ├── Color (Color)
    └── OutlineColor (Color)
```

### Settings Details

- **Delay** (Integer Range) — default: `0` – `0`; range: `0` – `40`; unit: ticks
- **MinDist** (Decimal) — default: `0.0`; range: `0.0` – `0.25`
- **Timer** (Decimal) — default: `1.0`; range: `0.01` – `10.0`
#### BlockItemSelection

A group of related settings.

- **Disallowed** (Registry List)
- **Unfavorable** (Registry List)

#### AutoBlock

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Always** (Toggle) — default: `false`
- **SlotResetDelay** (Integer) — default: `5`; range: `0` – `40`; unit: ticks
- **DoNotUseBelowCount** (Integer) — default: `1`; range: `0` – `64`

#### Prediction

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

#### Technique

Select a mode for this feature. Available modes: **Normal**, **Expand**, **GodBridge**, **Breezily**. Default: **Normal**.

##### Mode: Normal

- **RotationMode** (Choice) — default: `STABILIZED`; options: `Center`, `Random`, `Stabilized`, `NearestRotation`, `ReverseYaw`, `DiagonalYaw`, `AngleYaw`, `EdgePoint`
- **RequiresSight** (Toggle) — default: `false`
###### Eagle

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **BlocksToEagle** (Integer Range) — default: `0` – `0`; range: `0` – `10`
- **EdgeDistance** (Decimal) — default: `0.01`; range: `0.01` – `1.3`
- **OnlyOnGround** (Toggle) — default: `true`

###### Telly

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **ResetMode** (Choice) — default: `RESET`; options: `Reverse`, `Reset`
- **Straight** (Integer) — default: `0`; range: `0` – `5`; unit: ticks
- **Jump** (Integer Range) — default: `0` – `0`; range: `0` – `10`; unit: ticks
- **AimOnTower** (Toggle) — default: `true`

###### Down

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`

###### StabilizeMovement

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

###### Ceiling

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`

###### HeadHitter

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`


##### Mode: Expand

- **Length** (Integer) — default: `4`; range: `1` – `10`; unit: blocks

##### Mode: GodBridge

- **Modes** (Multi-Select) — default: `Jump`; options: `Jump`, `Sneak`, `StopInput`, `Backwards`
- **ForceSneakBelowCount** (Integer) — default: `3`; range: `0` – `10`
- **SneakTime** (Integer Range) — default: `1` – `1`; range: `1` – `10`

##### Mode: Breezily

- **EdgeDistance** (Decimal Range) — default: `0.45` – `0.5`; range: `0.25` – `0.5`; unit: blocks

- **SameY** (Choice) — default: `OFF`; options: `Off`, `On`, `Falling`, `Hypixel`
#### Tower

Select a mode for this feature. Available modes: **None**, **Motion**, **Pulldown**, **Karhu**, **Vulcan**, **Hypixel**. Default: **None**.

##### Mode: Motion

- **Motion** (Decimal) — default: `0.42`; range: `0.0` – `1.0`
- **TriggerHeight** (Decimal) — default: `0.78`; range: `0.76` – `1.0`
- **Slow** (Decimal) — default: `1.0`; range: `0.0` – `3.0`

##### Mode: Pulldown

- **Trigger** (Decimal) — default: `0.1`; range: `0.0` – `0.2`; unit: Y/v

##### Mode: Karhu

- **Timer** (Decimal) — default: `5.0`; range: `0.1` – `10.0`
- **Trigger** (Decimal) — default: `0.06`; range: `0.0` – `0.2`; unit: Y/v
- **Pulldown** (Toggle) — default: `true`

#### SafeWalk

Select a mode for this feature. Available modes: **None**, **Safe**, **OnEdge**. Default: **Safe**.

##### Mode: OnEdge

- **Distance** (Decimal) — default: `0.1`; range: `0.1` – `0.5`
- **Keep** (Integer Range) — default: `1` – `2`; range: `1` – `20`; unit: ticks
- **Mode** (Choice) — default: `STOP`; options: `Stop`, `Invert`, `Center`
- **Sneak** (Integer Range) — default: `0` – `0`; range: `0` – `20`; unit: ticks
- **Jump** (Toggle) — default: `false`

- **Swing** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
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
- **ConsiderInventory** (Toggle) — default: `false`
- **RotationTiming** (Choice) — default: `NORMAL`; options: `Normal`, `OnTick`, `OnTickSnap`

#### SprintControl

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Client** (Choice) — default: `DO_NOT_CHANGE`; options: `DoNotChange`, `ForceSprint`, `ForceNoSprint`, `NoSprintOnPlace`, `NoSprintOnGround`
- **Server** (Choice) — default: `DO_NOT_CHANGE`; options: `DoNotChange`, `ForceSprint`, `ForceNoSprint`, `NoSprintOnPlace`, `NoSprintOnGround`

#### SimulatePlacementAttempts

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
##### Clicker

A group of related settings.

- **CPS** (Integer Range) — default: `5` – `8`; range: `1` – `100`; unit: clicks
- **Technique** (Choice) — default: `STABILIZED`; options: `Stabilized`, `Efficient`, `Spamming`, `DoubleClick`, `Drag`, `Butterfly`, `NormalDistribution`

- **FailedAttemptsOnly** (Toggle) — default: `true`

#### Acceleration

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **SpeedMultiplier** (Decimal) — default: `0.6`; range: `0.1` – `3.0`
- **OnlyOnGround** (Toggle) — default: `false`

#### Strafe

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Speed** (Decimal) — default: `0.247`; range: `0.0` – `5.0`
- **Hypixel** (Toggle) — default: `false`
- **OnlyOnGround** (Toggle) — default: `false`

#### StrafeOnJump

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **StraightSpeed** (Decimal Range) — default: `0.48` – `0.49`; range: `0.1` – `1.0`
- **DiagonalSpeed** (Decimal Range) — default: `0.48` – `0.49`; range: `0.1` – `1.0`

#### SpeedLimiter

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **SpeedLimit** (Decimal) — default: `0.11`; range: `0.01` – `0.4`

#### Blink

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Time** (Integer Range) — default: `50` – `250`; range: `0` – `3000`; unit: ms
- **FlushOn** (Multi-Select) — options: `Place`, `Towering`, `Sneaking`, `NotSneaking`, `OnGround`, `InAir`

- **AutoSpeed** (Toggle) — default: `false`
- **Ledge** (Toggle) — default: `true`
#### Render

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Clump** (Toggle) — default: `true`
- **StartSize** (Decimal) — default: `1.0`; range: `0.0` – `2.0`
- **StartCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **EndSize** (Decimal) — default: `0.8`; range: `0.0` – `2.0`
- **EndCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **FadeInCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **FadeOutCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **InTime** (Integer) — default: `500`; range: `0` – `5000`; unit: ms
- **OutTime** (Integer) — default: `500`; range: `0` – `5000`; unit: ms
- **Color** (Color)
- **OutlineColor** (Color)


### Screenshots

*Screenshots for Scaffold will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2FModuleScaffold.kt)*
