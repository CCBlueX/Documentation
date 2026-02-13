## CrystalAura

Automatically places and destroys end crystals.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Target (Setting Group)
│   ├── Range (Decimal | default: 4.5 | range: 1.0..12.0)
│   ├── FOV (Decimal | default: 180.0 | range: 0.0..180.0)
│   ├── HurtTime (Integer | default: 10 | range: 0..10)
│   └── Priority (Multi-Select | default: [Type, Health] | options: Type, Health, Distance, Direction, HurtTime, Age)
├── Place (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Swing (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│   ├── Switch (Choice | default: SILENT | options: Silent, Normal, None)
│   ├── 1_12_2 (Toggle | default: false)
│   ├── Delay (Integer | default: 0 | range: 0..1000 | ms)
│   ├── Range (Decimal | default: 4.5 | range: 1.0..6.0)
│   ├── WallsRange (Decimal | default: 4.5 | range: 0.0..6.0)
│   ├── OnlyAbove (Toggle | default: false)
│   ├── Sequenced (Toggle | default: false)
│   ├── NotFacingAway (Toggle | default: false)
│   ├── Jitter (Toggle | default: false)
│   └── TargetRendering (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       ├── Clump (Toggle | default: false)
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
├── Destroy (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Swing (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│   ├── Delay (Integer | default: 0 | range: 0..1000 | ms)
│   ├── Range (Decimal | default: 4.5 | range: 1.0..6.0)
│   ├── WallsRange (Decimal | default: 4.5 | range: 0.0..6.0)
│   └── PrioritizeVisibleFaces (Toggle | default: false)
├── Damage (Setting Group)
│   ├── MaxSelfDamage (Decimal | default: 2.0 | range: 0.0..10.0)
│   ├── MaxFriendDamage (Decimal | default: 1.0 | range: 0.0..10.0)
│   ├── MinEnemyDamage (Decimal | default: 5.0 | range: 0.0..10.0)
│   ├── AntiSuicide (Toggle | default: true)
│   ├── Efficient (Toggle | default: true)
│   └── Terrain (Toggle | default: true)
├── Triggers (Setting Group)
│   ├── NotWhileUsingItem (Toggle | default: false)
│   ├── Off-Thread (Toggle | default: true)
│   ├── Tick (Toggle | default: true)
│   ├── BlockChange (Toggle | default: true)
│   ├── ClientBlockBreak (Toggle | default: true)
│   ├── CrystalSpawn (Toggle | default: true)
│   ├── CrystalDestroy (Toggle | default: true)
│   ├── ExplodeSound (Toggle | default: true)
│   ├── EntityMove (Toggle | default: true)
│   └── SelfMove (Toggle | default: false)
├── Predict (Setting Group)
│   ├── Self (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   ├── PlaceTicks (Integer | default: 2 | range: 0..20)
│   │   ├── BreakTicks (Integer | default: 1 | range: 0..20)
│   │   ├── BasePlaceTicks (Integer | default: 4 | range: 0..20)
│   │   ├── CalculationMode (Mode Selector | default: Both | modes: Both, PredictOnly)
│   │   │   ├── [Mode: Both]
│   │   │   │   └── Logic (Choice | default: AND | options: And, Or)
│   │   └── CheckIntersect (Toggle | default: true)
│   └── Target (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       ├── PlaceTicks (Integer | default: 2 | range: 0..20)
│       ├── BreakTicks (Integer | default: 1 | range: 0..20)
│       ├── BasePlaceTicks (Integer | default: 4 | range: 0..20)
│       ├── CalculationMode (Mode Selector | default: Both | modes: Both, PredictOnly)
│       │   ├── [Mode: Both]
│       │   │   └── Logic (Choice | default: AND | options: And, Or)
│       └── CheckIntersect (Toggle | default: true)
├── IDPredict (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── OffsetRange (Integer Range | default: 1..2 | range: 1..100)
│   ├── SwingAlways (Toggle | default: false)
│   └── Rotate (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       └── Back (Toggle | default: false)
├── SetDead (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── ConfirmTime (Integer | default: 150 | range: 10..2000 | ms)
├── BasePlace (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── CalcDelay (Integer | default: 120 | range: 0..1000 | ms)
│   ├── TimeOut (Integer | default: 240 | range: 0..5000 | ms)
│   ├── PlatformOnly (Toggle | default: false)
│   ├── OnlyAboveSelf (Toggle | default: false)
│   ├── Terrain (Toggle | default: true)
│   ├── SimulateMovement (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   ├── Ticks (Integer | default: 3 | range: 1..20)
│   │   ├── Error (Decimal | default: 0.1 | range: 0.0..2.0)
│   │   ├── ErrorStep (Decimal | default: 0.05 | range: 0.0..1.0)
│   │   ├── DownError (Toggle | default: false)
│   │   └── AntiPlatformSimulate (Toggle | default: true)
│   ├── MinAdvantage (Decimal | default: 2.0 | range: 0.1..10.0)
│   └── Placing (Setting Group)
│       ├── Range (Decimal | default: 4.5 | range: 1.0..6.0)
│       ├── WallRange (Decimal | default: 4.5 | range: 0.0..6.0)
│       ├── Cooldown (Integer Range | default: 1..2 | range: 0..40 | ticks)
│       ├── Swing (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│       ├── ConstructFailResult (Toggle | default: true)
│       ├── Sneak (Integer | default: 1 | range: 0..10 | ticks)
│       ├── Ignore (Multi-Select | default: [OpenInventory, UsingItem] | options: OpenInventory, UsingItem)
│       ├── SlotResetDelay (Integer Range | default: 4..6 | range: 0..40 | ticks)
│       ├── RotationMode (Mode Selector | default: Normal | modes: Normal, None)
│       │   ├── [Mode: Normal]
│       │   │   ├── PostMove (Toggle | default: false)
│       │   │   └── Rotations (Setting Group)
│       │   │       ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│       │   │       │   ├── [Mode: Linear]
│       │   │       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   │       │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   │       │   ├── [Mode: Sigmoid]
│       │   │       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   │       │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │   │       │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│       │   │       │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│       │   │       │   └── [Mode: Acceleration]
│       │   │       │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│       │   │       │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│       │   │       │       ├── DynamicAccel (Toggleable Group | default: off)
│       │   │       │       │   ├── Enabled (Toggle | default: false)
│       │   │       │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│       │   │       │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│       │   │       │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│       │   │       │       ├── AccelerationError (Toggleable Group | default: on)
│       │   │       │       │   ├── Enabled (Toggle | default: true)
│       │   │       │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │   │       │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │   │       │       ├── ConstantError (Toggleable Group | default: on)
│       │   │       │       │   ├── Enabled (Toggle | default: true)
│       │   │       │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │   │       │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │   │       │       └── SigmoidDeceleration (Toggleable Group | default: off)
│       │   │       │           ├── Enabled (Toggle | default: false)
│       │   │       │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│       │   │       │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│       │   │       ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│       │   │       ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│       │   │       └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│       │   └── [Mode: None]
│       │       ├── PostMove (Toggle | default: false)
│       │       ├── SendRotationPacket (Toggle | default: false)
│       │       └── Placements (Integer | default: 1 | range: 1..10 | b/o)
│       ├── Support (Toggleable Group | default: on)
│       │   ├── Enabled (Toggle | default: true)
│       │   ├── Depth (Integer | default: 4 | range: 1..12)
│       │   ├── Delay (Integer | default: 500 | range: 0..1000 | ms)
│       │   ├── Filter (Choice | default: BLACKLIST | options: Whitelist, Blacklist)
│       │   └── Blocks (Registry List)
│       ├── DestroyCrystals (Toggleable Group | default: on)
│       │   ├── Enabled (Toggle | default: true)
│       │   ├── Range (Decimal | default: 4.5 | range: 1.0..6.0)
│       │   ├── WallRange (Decimal | default: 4.5 | range: 0.0..6.0)
│       │   ├── Delay (Integer | default: 0 | range: 0..1000 | ms)
│       │   ├── SwingMode (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│       │   └── RotationMode (Mode Selector | default: Normal | modes: Normal, None)
│       │       ├── [Mode: Normal]
│       │       │   ├── PostMove (Toggle | default: false)
│       │       │   ├── Instant (Toggle | default: false)
│       │       │   ├── Rotations (Setting Group)
│       │       │   │   ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│       │       │   │   │   ├── [Mode: Linear]
│       │       │   │   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │       │   │   │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │       │   │   │   ├── [Mode: Sigmoid]
│       │       │   │   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │       │   │   │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       │       │   │   │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│       │       │   │   │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│       │       │   │   │   └── [Mode: Acceleration]
│       │       │   │   │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│       │       │   │   │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│       │       │   │   │       ├── DynamicAccel (Toggleable Group | default: off)
│       │       │   │   │       │   ├── Enabled (Toggle | default: false)
│       │       │   │   │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│       │       │   │   │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│       │       │   │   │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│       │       │   │   │       ├── AccelerationError (Toggleable Group | default: on)
│       │       │   │   │       │   ├── Enabled (Toggle | default: true)
│       │       │   │   │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       │   │   │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       │   │   │       ├── ConstantError (Toggleable Group | default: on)
│       │       │   │   │       │   ├── Enabled (Toggle | default: true)
│       │       │   │   │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       │   │   │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│       │       │   │   │       └── SigmoidDeceleration (Toggleable Group | default: off)
│       │       │   │   │           ├── Enabled (Toggle | default: false)
│       │       │   │   │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│       │       │   │   │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│       │       │   │   ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│       │       │   │   ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│       │       │   │   └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│       │       │   └── IgnoreOpenInventory (Toggle | default: true)
│       │       └── [Mode: None]
│       │           ├── PostMove (Toggle | default: false)
│       │           ├── Instant (Toggle | default: false)
│       │           └── SendRotationPacket (Toggle | default: false)
│       ├── TargetRendering (Toggleable Group | default: off)
│       │   ├── Enabled (Toggle | default: false)
│       │   ├── Clump (Toggle | default: true)
│       │   ├── StartSize (Decimal | default: 1.0 | range: 0.0..2.0)
│       │   ├── StartCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│       │   ├── EndSize (Decimal | default: 0.8 | range: 0.0..2.0)
│       │   ├── EndCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│       │   ├── FadeInCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│       │   ├── FadeOutCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│       │   ├── InTime (Integer | default: 500 | range: 0..5000 | ms)
│       │   ├── OutTime (Integer | default: 500 | range: 0..5000 | ms)
│       │   ├── Color (Color)
│       │   └── OutlineColor (Color)
│       └── PlacedRendering (Toggleable Group | default: on)
│           ├── Enabled (Toggle | default: true)
│           ├── Clump (Toggle | default: true)
│           ├── StartSize (Decimal | default: 1.0 | range: 0.0..2.0)
│           ├── StartCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│           ├── EndSize (Decimal | default: 0.8 | range: 0.0..2.0)
│           ├── EndCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│           ├── FadeInCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│           ├── FadeOutCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
│           ├── InTime (Integer | default: 500 | range: 0..5000 | ms)
│           ├── OutTime (Integer | default: 500 | range: 0..5000 | ms)
│           ├── Color (Color)
│           └── OutlineColor (Color)
├── TargetRendering (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Mode (Mode Selector | default: Image | modes: Legacy, Circle, Image, GlowingCircle, Ghost, Text2D, Arrow)
│       ├── [Mode: Legacy]
│       │   ├── Size (Decimal | default: 0.5 | range: 0.1..2.0)
│       │   ├── Height (Decimal | default: 0.1 | range: 0.02..2.0)
│       │   ├── Color (Color)
│       │   └── ExtraYOffset (Decimal | default: 0.1 | range: 0.0..1.0)
│       ├── [Mode: Circle]
│       │   ├── Radius (Decimal | default: 0.85 | range: 0.1..2.0)
│       │   ├── InnerRadius (Decimal | default: 0.0 | range: 0.0..2.0)
│       │   ├── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
│       │   │   ├── [Mode: Feet]
│       │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│       │   │   ├── [Mode: Top]
│       │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│       │   │   ├── [Mode: Relative]
│       │   │   │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
│       │   │   └── [Mode: Animated]
│       │   │       ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
│       │   │       ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
│       │   │       ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
│       │   │       └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
│       │   ├── OuterColor (Color)
│       │   ├── InnerColor (Color)
│       │   └── Color (Color)
│       ├── [Mode: Image]
│       │   ├── Source (Mode Selector | default: Custom | modes: Custom, Builtin)
│       │   │   ├── [Mode: Custom]
│       │   │   │   └── File (File)
│       │   │   └── [Mode: Builtin]
│       │   │       └── Preset (Choice | default: MARKER1 | options: Marker1, Marker2)
│       │   ├── Scale (2D Position)
│       │   ├── ColorModulator (Color)
│       │   ├── Rotate (Setting Group)
│       │   │   ├── Period (Integer | default: 1000 | range: 10..20000 | ms)
│       │   │   ├── Symmetric (Toggle | default: true)
│       │   │   └── Curve (Curve)
│       │   └── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
│       │       ├── [Mode: Feet]
│       │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│       │       ├── [Mode: Top]
│       │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│       │       ├── [Mode: Relative]
│       │       │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
│       │       └── [Mode: Animated]
│       │           ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
│       │           ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
│       │           ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
│       │           └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
│       ├── [Mode: GlowingCircle]
│       │   ├── Radius (Decimal | default: 0.85 | range: 0.1..2.0)
│       │   ├── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
│       │   │   ├── [Mode: Feet]
│       │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│       │   │   ├── [Mode: Top]
│       │   │   │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│       │   │   ├── [Mode: Relative]
│       │   │   │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
│       │   │   └── [Mode: Animated]
│       │   │       ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
│       │   │       ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
│       │   │       ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
│       │   │       └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
│       │   ├── OuterColor (Color)
│       │   ├── GlowColor (Color)
│       │   ├── GlowHeight (Decimal | default: 0.3 | range: -1.0..1.0)
│       │   └── Color (Color)
│       ├── [Mode: Ghost]
│       │   ├── Color (Color)
│       │   ├── Size (Decimal | default: 0.5 | range: 0.4..0.7)
│       │   └── Length (Integer | default: 25 | range: 15..40)
│       ├── [Mode: Text2D]
│       │   ├── Scale (Decimal | default: 1.0 | range: 0.01..10.0)
│       │   ├── Shadow (Toggle | default: true)
│       │   ├── Color (Color)
│       │   ├── Text (Editable List)
│       │   └── HeightMode (Mode Selector | default: Feet | modes: Feet, Top, Relative, Health, Animated)
│       │       ├── [Mode: Feet]
│       │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│       │       ├── [Mode: Top]
│       │       │   └── Offset (Decimal | default: 0.0 | range: -1.0..1.0)
│       │       ├── [Mode: Relative]
│       │       │   └── Height (Decimal | default: 0.5 | range: -0.5..1.5)
│       │       └── [Mode: Animated]
│       │           ├── Speed (Decimal | default: 0.18 | range: 0.01..1.0)
│       │           ├── HeightMultiplier (Decimal | default: 0.4 | range: 0.1..1.0)
│       │           ├── HeightOffset (Decimal | default: 1.3 | range: 0.0..2.0)
│       │           └── GlowOffset (Decimal | default: -1.0 | range: -3.1..3.1)
│       └── [Mode: Arrow]
│           ├── Color (Color)
│           ├── OutlineColor (Color)
│           └── Size (Decimal | default: 1.5 | range: 0.5..20.0)
└── RotationMode (Mode Selector | default: Normal | modes: Normal, None)
    ├── [Mode: Normal]
    │   ├── PostMove (Toggle | default: false)
    │   ├── Instant (Toggle | default: false)
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
    │   └── IgnoreOpenInventory (Toggle | default: true)
    └── [Mode: None]
        ├── PostMove (Toggle | default: false)
        ├── Instant (Toggle | default: false)
        └── SendRotationPacket (Toggle | default: false)
```

### Settings Details

#### Target

A group of related settings.

- **Range** (Decimal) — default: `4.5`; range: `1.0` – `12.0`
- **FOV** (Decimal) — default: `180.0`; range: `0.0` – `180.0`
- **HurtTime** (Integer) — default: `10`; range: `0` – `10`
- **Priority** (Multi-Select) — default: `Type`, `Health`; options: `Type`, `Health`, `Distance`, `Direction`, `HurtTime`, `Age`

#### Place

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Swing** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **Switch** (Choice) — default: `SILENT`; options: `Silent`, `Normal`, `None`
- **1_12_2** (Toggle) — default: `false`
- **Delay** (Integer) — default: `0`; range: `0` – `1000`; unit: ms
- **Range** (Decimal) — default: `4.5`; range: `1.0` – `6.0`
- **WallsRange** (Decimal) — default: `4.5`; range: `0.0` – `6.0`
- **OnlyAbove** (Toggle) — default: `false`
- **Sequenced** (Toggle) — default: `false`
- **NotFacingAway** (Toggle) — default: `false`
- **Jitter** (Toggle) — default: `false`
##### TargetRendering

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Clump** (Toggle) — default: `false`
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


#### Destroy

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Swing** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **Delay** (Integer) — default: `0`; range: `0` – `1000`; unit: ms
- **Range** (Decimal) — default: `4.5`; range: `1.0` – `6.0`
- **WallsRange** (Decimal) — default: `4.5`; range: `0.0` – `6.0`
- **PrioritizeVisibleFaces** (Toggle) — default: `false`

#### Damage

A group of related settings.

- **MaxSelfDamage** (Decimal) — default: `2.0`; range: `0.0` – `10.0`
- **MaxFriendDamage** (Decimal) — default: `1.0`; range: `0.0` – `10.0`
- **MinEnemyDamage** (Decimal) — default: `5.0`; range: `0.0` – `10.0`
- **AntiSuicide** (Toggle) — default: `true`
- **Efficient** (Toggle) — default: `true`
- **Terrain** (Toggle) — default: `true`

#### Triggers

A group of related settings.

- **NotWhileUsingItem** (Toggle) — default: `false`
- **Off-Thread** (Toggle) — default: `true`
- **Tick** (Toggle) — default: `true`
- **BlockChange** (Toggle) — default: `true`
- **ClientBlockBreak** (Toggle) — default: `true`
- **CrystalSpawn** (Toggle) — default: `true`
- **CrystalDestroy** (Toggle) — default: `true`
- **ExplodeSound** (Toggle) — default: `true`
- **EntityMove** (Toggle) — default: `true`
- **SelfMove** (Toggle) — default: `false`

#### Predict

A group of related settings.

##### Self

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **PlaceTicks** (Integer) — default: `2`; range: `0` – `20`
- **BreakTicks** (Integer) — default: `1`; range: `0` – `20`
- **BasePlaceTicks** (Integer) — default: `4`; range: `0` – `20`
###### CalculationMode

Select a mode for this feature. Available modes: **Both**, **PredictOnly**. Default: **Both**.

###### Mode: Both

- **Logic** (Choice) — default: `AND`; options: `And`, `Or`

- **CheckIntersect** (Toggle) — default: `true`

##### Target

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **PlaceTicks** (Integer) — default: `2`; range: `0` – `20`
- **BreakTicks** (Integer) — default: `1`; range: `0` – `20`
- **BasePlaceTicks** (Integer) — default: `4`; range: `0` – `20`
###### CalculationMode

Select a mode for this feature. Available modes: **Both**, **PredictOnly**. Default: **Both**.

###### Mode: Both

- **Logic** (Choice) — default: `AND`; options: `And`, `Or`

- **CheckIntersect** (Toggle) — default: `true`


#### IDPredict

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **OffsetRange** (Integer Range) — default: `1` – `2`; range: `1` – `100`
- **SwingAlways** (Toggle) — default: `false`
##### Rotate

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Back** (Toggle) — default: `false`


#### SetDead

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **ConfirmTime** (Integer) — default: `150`; range: `10` – `2000`; unit: ms

#### BasePlace

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **CalcDelay** (Integer) — default: `120`; range: `0` – `1000`; unit: ms
- **TimeOut** (Integer) — default: `240`; range: `0` – `5000`; unit: ms
- **PlatformOnly** (Toggle) — default: `false`
- **OnlyAboveSelf** (Toggle) — default: `false`
- **Terrain** (Toggle) — default: `true`
##### SimulateMovement

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Ticks** (Integer) — default: `3`; range: `1` – `20`
- **Error** (Decimal) — default: `0.1`; range: `0.0` – `2.0`
- **ErrorStep** (Decimal) — default: `0.05`; range: `0.0` – `1.0`
- **DownError** (Toggle) — default: `false`
- **AntiPlatformSimulate** (Toggle) — default: `true`

- **MinAdvantage** (Decimal) — default: `2.0`; range: `0.1` – `10.0`
##### Placing

A group of related settings.

- **Range** (Decimal) — default: `4.5`; range: `1.0` – `6.0`
- **WallRange** (Decimal) — default: `4.5`; range: `0.0` – `6.0`
- **Cooldown** (Integer Range) — default: `1` – `2`; range: `0` – `40`; unit: ticks
- **Swing** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **ConstructFailResult** (Toggle) — default: `true`
- **Sneak** (Integer) — default: `1`; range: `0` – `10`; unit: ticks
- **Ignore** (Multi-Select) — default: `OpenInventory`, `UsingItem`; options: `OpenInventory`, `UsingItem`
- **SlotResetDelay** (Integer Range) — default: `4` – `6`; range: `0` – `40`; unit: ticks
###### RotationMode

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

###### Support

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Depth** (Integer) — default: `4`; range: `1` – `12`
- **Delay** (Integer) — default: `500`; range: `0` – `1000`; unit: ms
- **Filter** (Choice) — default: `BLACKLIST`; options: `Whitelist`, `Blacklist`
- **Blocks** (Registry List)

###### DestroyCrystals

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


###### TargetRendering

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

###### PlacedRendering

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


#### RotationMode

Select a mode for this feature. Available modes: **Normal**, **None**. Default: **Normal**.

##### Mode: Normal

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

##### Mode: None

- **PostMove** (Toggle) — default: `false`
- **Instant** (Toggle) — default: `false`
- **SendRotationPacket** (Toggle) — default: `false`


### Screenshots

*Screenshots for CrystalAura will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleCrystalAura.kt)*
