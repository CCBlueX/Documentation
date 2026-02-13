## BedDefender

Automatically places blocks to defend your bed in BedWars.

**Category:** World  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── MaxLayers (Integer | default: 1 | range: 1..5)
├── SelfBed (Mode Selector | default: None | modes: None, Color, SpawnLocation, Manual)
│   ├── [Mode: Color]
│   │   └── Slots (Multi-Select | default: [Head] | options: Feet, Legs, Chest, Head)
│   ├── [Mode: SpawnLocation]
│   │   └── BedDistance (Decimal | default: 24.0 | range: 16.0..48.0)
│   └── [Mode: Manual]
│       ├── Track (Key)
│       └── Untrack (Key)
├── Place (Setting Group)
│   ├── Range (Decimal | default: 4.5 | range: 1.0..6.0)
│   ├── WallRange (Decimal | default: 4.5 | range: 0.0..6.0)
│   ├── Cooldown (Integer Range | default: 1..2 | range: 0..40 | ticks)
│   ├── Swing (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│   ├── ConstructFailResult (Toggle | default: true)
│   ├── Sneak (Integer | default: 1 | range: 0..10 | ticks)
│   ├── Ignore (Multi-Select | default: [OpenInventory, UsingItem] | options: OpenInventory, UsingItem)
│   ├── SlotResetDelay (Integer Range | default: 4..6 | range: 0..40 | ticks)
│   ├── RotationMode (Mode Selector | default: Normal | modes: Normal, None)
│   │   ├── [Mode: Normal]
│   │   │   ├── PostMove (Toggle | default: false)
│   │   │   └── Rotations (Setting Group)
│   │   │       ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│   │   │       │   ├── [Mode: Linear]
│   │   │       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │       │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │       │   ├── [Mode: Sigmoid]
│   │   │       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │       │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │       │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │       │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   │       │   └── [Mode: Acceleration]
│   │   │       │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │       │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │       │       ├── DynamicAccel (Toggleable Group | default: off)
│   │   │       │       │   ├── Enabled (Toggle | default: false)
│   │   │       │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│   │   │       │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │       │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │       │       ├── AccelerationError (Toggleable Group | default: on)
│   │   │       │       │   ├── Enabled (Toggle | default: true)
│   │   │       │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │       │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │       │       ├── ConstantError (Toggleable Group | default: on)
│   │   │       │       │   ├── Enabled (Toggle | default: true)
│   │   │       │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │       │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │       │       └── SigmoidDeceleration (Toggleable Group | default: off)
│   │   │       │           ├── Enabled (Toggle | default: false)
│   │   │       │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │       │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   │       ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│   │   │       ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│   │   │       └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│   │   └── [Mode: None]
│   │       ├── PostMove (Toggle | default: false)
│   │       ├── SendRotationPacket (Toggle | default: false)
│   │       └── Placements (Integer | default: 1 | range: 1..10 | b/o)
│   ├── DestroyCrystals (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   ├── Range (Decimal | default: 4.5 | range: 1.0..6.0)
│   │   ├── WallRange (Decimal | default: 4.5 | range: 0.0..6.0)
│   │   ├── Delay (Integer | default: 0 | range: 0..1000 | ms)
│   │   ├── SwingMode (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│   │   └── RotationMode (Mode Selector | default: Normal | modes: Normal, None)
│   │       ├── [Mode: Normal]
│   │       │   ├── PostMove (Toggle | default: false)
│   │       │   ├── Instant (Toggle | default: false)
│   │       │   ├── Rotations (Setting Group)
│   │       │   │   ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│   │       │   │   │   ├── [Mode: Linear]
│   │       │   │   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │       │   │   │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │       │   │   │   ├── [Mode: Sigmoid]
│   │       │   │   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │       │   │   │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │       │   │   │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │       │   │   │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │       │   │   │   └── [Mode: Acceleration]
│   │       │   │   │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │       │   │   │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │       │   │   │       ├── DynamicAccel (Toggleable Group | default: off)
│   │       │   │   │       │   ├── Enabled (Toggle | default: false)
│   │       │   │   │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│   │       │   │   │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │       │   │   │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │       │   │   │       ├── AccelerationError (Toggleable Group | default: on)
│   │       │   │   │       │   ├── Enabled (Toggle | default: true)
│   │       │   │   │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       │   │   │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       │   │   │       ├── ConstantError (Toggleable Group | default: on)
│   │       │   │   │       │   ├── Enabled (Toggle | default: true)
│   │       │   │   │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       │   │   │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       │   │   │       └── SigmoidDeceleration (Toggleable Group | default: off)
│   │       │   │   │           ├── Enabled (Toggle | default: false)
│   │       │   │   │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │       │   │   │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │       │   │   ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│   │       │   │   ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│   │       │   │   └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│   │       │   └── IgnoreOpenInventory (Toggle | default: true)
│   │       └── [Mode: None]
│   │           ├── PostMove (Toggle | default: false)
│   │           ├── Instant (Toggle | default: false)
│   │           └── SendRotationPacket (Toggle | default: false)
│   ├── TargetRendering (Toggleable Group | default: off)
│   │   ├── Enabled (Toggle | default: false)
│   │   ├── Clump (Toggle | default: true)
│   │   ├── StartSize (Decimal | default: 1.0 | range: 0.0..2.0)
│   │   ├── StartCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│   │   ├── EndSize (Decimal | default: 0.8 | range: 0.0..2.0)
│   │   ├── EndCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│   │   ├── FadeInCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│   │   ├── FadeOutCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│   │   ├── InTime (Integer | default: 500 | range: 0..5000 | ms)
│   │   ├── OutTime (Integer | default: 500 | range: 0..5000 | ms)
│   │   ├── Color (Color)
│   │   └── OutlineColor (Color)
│   └── PlacedRendering (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       ├── Clump (Toggle | default: true)
│       ├── StartSize (Decimal | default: 1.0 | range: 0.0..2.0)
│       ├── StartCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│       ├── EndSize (Decimal | default: 0.8 | range: 0.0..2.0)
│       ├── EndCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│       ├── FadeInCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│       ├── FadeOutCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│       ├── InTime (Integer | default: 500 | range: 0..5000 | ms)
│       ├── OutTime (Integer | default: 500 | range: 0..5000 | ms)
│       ├── Color (Color)
│       └── OutlineColor (Color)
└── RequiresSneak (Toggle | default: false)
```

### Settings Details

- **MaxLayers** (Integer) — default: `1`; range: `1` – `5`
#### SelfBed

Select a mode for this feature. Available modes: **None**, **Color**, **SpawnLocation**, **Manual**. Default: **None**.

##### Mode: Color

- **Slots** (Multi-Select) — default: `Head`; options: `Feet`, `Legs`, `Chest`, `Head`

##### Mode: SpawnLocation

- **BedDistance** (Decimal) — default: `24.0`; range: `16.0` – `48.0`

##### Mode: Manual

- **Track** (Key)
- **Untrack** (Key)

#### Place

A group of related settings.

- **Range** (Decimal) — default: `4.5`; range: `1.0` – `6.0`
- **WallRange** (Decimal) — default: `4.5`; range: `0.0` – `6.0`
- **Cooldown** (Integer Range) — default: `1` – `2`; range: `0` – `40`; unit: ticks
- **Swing** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **ConstructFailResult** (Toggle) — default: `true`
- **Sneak** (Integer) — default: `1`; range: `0` – `10`; unit: ticks
- **Ignore** (Multi-Select) — default: `OpenInventory`, `UsingItem`; options: `OpenInventory`, `UsingItem`
- **SlotResetDelay** (Integer Range) — default: `4` – `6`; range: `0` – `40`; unit: ticks
##### RotationMode

Select a mode for this feature. Available modes: **Normal**, **None**. Default: **Normal**.

###### Mode: Normal

- **PostMove** (Toggle) — default: `false`
###### Rotations

A group of related settings.

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


###### Mode: None

- **PostMove** (Toggle) — default: `false`
- **SendRotationPacket** (Toggle) — default: `false`
- **Placements** (Integer) — default: `1`; range: `1` – `10`; unit: b/o

##### DestroyCrystals

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Range** (Decimal) — default: `4.5`; range: `1.0` – `6.0`
- **WallRange** (Decimal) — default: `4.5`; range: `0.0` – `6.0`
- **Delay** (Integer) — default: `0`; range: `0` – `1000`; unit: ms
- **SwingMode** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
###### RotationMode

Select a mode for this feature. Available modes: **Normal**, **None**. Default: **Normal**.

###### Mode: Normal

- **PostMove** (Toggle) — default: `false`
- **Instant** (Toggle) — default: `false`
###### Rotations

A group of related settings.

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

- **IgnoreOpenInventory** (Toggle) — default: `true`

###### Mode: None

- **PostMove** (Toggle) — default: `false`
- **Instant** (Toggle) — default: `false`
- **SendRotationPacket** (Toggle) — default: `false`


##### TargetRendering

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
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

##### PlacedRendering

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


- **RequiresSneak** (Toggle) — default: `false`

### Screenshots

*Screenshots for BedDefender will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2FModuleBedDefender.kt)*
