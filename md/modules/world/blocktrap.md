## BlockTrap

Traps enemies in blocks.

**Category:** World  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── DoublePlace (Multi-Select | options: Above, Below)
├── PlaceAt (Multi-Select | default: [Legs, Floor] | options: Legs, Floor)
├── Instant (Toggle | default: true)
├── Filter (Choice | default: BLACKLIST | options: Whitelist, Blacklist)
├── Blocks (Registry List)
├── PlacePriority (Choice | default: FURTHEST | options: Closest, Furthest, Highest, Lowest)
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
│   ├── Support (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   ├── Depth (Integer | default: 4 | range: 1..12)
│   │   ├── Delay (Integer | default: 500 | range: 0..1000 | ms)
│   │   ├── Filter (Choice | default: BLACKLIST | options: Whitelist, Blacklist)
│   │   └── Blocks (Registry List)
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
├── Target (Setting Group)
│   ├── Range (Decimal | default: 4.0 | range: 1.0..6.0)
│   ├── FOV (Decimal | default: 180.0 | range: 0.0..180.0)
│   ├── HurtTime (Integer | default: 10 | range: 0..10)
│   └── Priority (Multi-Select | default: [Type, Direction] | options: Type, Health, Distance, Direction, HurtTime, Age)
└── TargetRendering (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    └── Mode (Mode Selector | default: Image | modes: Legacy, Circle, Image, GlowingCircle, Ghost, Text2D, Arrow)
        ├── [Mode: Legacy]
        │   ├── Size (Decimal | default: 0.5 | range: 0.1..2.0)
        │   ├── Height (Decimal | default: 0.1 | range: 0.02..2.0)
        │   ├── Color (Color)
        │   └── ExtraYOffset (Decimal | default: 0.1 | range: 0.0..1.0)
        ├── [Mode: Circle]
        │   ├── Radius (Decimal | default: 0.85 | range: 0.1..2.0)
        │   ├── InnerRadius (Decimal | default: 0.0 | range: 0.0..2.0)
        │   ├── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
        │   │   ├── [Mode: Feet]
        │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
        │   │   ├── [Mode: Top]
        │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
        │   │   ├── [Mode: Relative]
        │   │   │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
        │   │   └── [Mode: Animated]
        │   │       ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
        │   │       ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
        │   │       ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
        │   │       └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
        │   ├── OuterColor (Color)
        │   ├── InnerColor (Color)
        │   └── Color (Color)
        ├── [Mode: Image]
        │   ├── Source (Mode Selector | default: Custom | modes: Custom, Builtin)
        │   │   ├── [Mode: Custom]
        │   │   │   └── File (File)
        │   │   └── [Mode: Builtin]
        │   │       └── Preset (Choice | default: MARKER1 | options: Marker1, Marker2)
        │   ├── Scale (2D Position)
        │   ├── ColorModulator (Color)
        │   ├── Rotate (Setting Group)
        │   │   ├── Period (Integer | default: 1000 | range: 10..20000 | ms)
        │   │   ├── Symmetric (Toggle | default: true)
        │   │   └── Curve (Curve)
        │   └── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
        │       ├── [Mode: Feet]
        │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
        │       ├── [Mode: Top]
        │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
        │       ├── [Mode: Relative]
        │       │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
        │       └── [Mode: Animated]
        │           ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
        │           ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
        │           ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
        │           └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
        ├── [Mode: GlowingCircle]
        │   ├── Radius (Decimal | default: 0.85 | range: 0.1..2.0)
        │   ├── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
        │   │   ├── [Mode: Feet]
        │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
        │   │   ├── [Mode: Top]
        │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
        │   │   ├── [Mode: Relative]
        │   │   │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
        │   │   └── [Mode: Animated]
        │   │       ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
        │   │       ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
        │   │       ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
        │   │       └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
        │   ├── OuterColor (Color)
        │   ├── GlowColor (Color)
        │   ├── GlowHeight (Decimal | default: 0.3 | range: -1.0..1.0)
        │   └── Color (Color)
        ├── [Mode: Ghost]
        │   ├── Color (Color)
        │   ├── Size (Decimal | default: 0.5 | range: 0.4..0.7)
        │   └── Length (Integer | default: 25 | range: 15..40)
        ├── [Mode: Text2D]
        │   ├── Scale (Decimal | default: 1.0 | range: 0.01..10.0)
        │   ├── Shadow (Toggle | default: true)
        │   ├── Color (Color)
        │   ├── Text (Editable List)
        │   └── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
        │       ├── [Mode: Feet]
        │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
        │       ├── [Mode: Top]
        │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
        │       ├── [Mode: Relative]
        │       │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
        │       └── [Mode: Animated]
        │           ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
        │           ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
        │           ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
        │           └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
        └── [Mode: Arrow]
            ├── Color (Color)
            ├── OutlineColor (Color)
            └── Size (Decimal | default: 1.5 | range: 0.5..20.0)
```

### Settings Details

- **DoublePlace** (Multi-Select) — options: `Above`, `Below`
- **PlaceAt** (Multi-Select) — default: `Legs`, `Floor`; options: `Legs`, `Floor`
- **Instant** (Toggle) — default: `true`
- **Filter** (Choice) — default: `BLACKLIST`; options: `Whitelist`, `Blacklist`
- **Blocks** (Registry List)
- **PlacePriority** (Choice) — default: `FURTHEST`; options: `Closest`, `Furthest`, `Highest`, `Lowest`
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

##### Support

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Depth** (Integer) — default: `4`; range: `1` – `12`
- **Delay** (Integer) — default: `500`; range: `0` – `1000`; unit: ms
- **Filter** (Choice) — default: `BLACKLIST`; options: `Whitelist`, `Blacklist`
- **Blocks** (Registry List)

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


#### Target

A group of related settings.

- **Range** (Decimal) — default: `4.0`; range: `1.0` – `6.0`
- **FOV** (Decimal) — default: `180.0`; range: `0.0` – `180.0`
- **HurtTime** (Integer) — default: `10`; range: `0` – `10`
- **Priority** (Multi-Select) — default: `Type`, `Direction`; options: `Type`, `Health`, `Distance`, `Direction`, `HurtTime`, `Age`

#### TargetRendering

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### Mode

Select a mode for this feature. Available modes: **Legacy**, **Circle**, **Image**, **GlowingCircle**, **Ghost**, **Text2D**, **Arrow**. Default: **Image**.

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



### Screenshots

*Screenshots for BlockTrap will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2FModuleBlockTrap.kt)*
