## KillAura

Automatically attacks enemies around you.

**Category:** Combat  
**Enabled by default:** No  

### Frequently Asked Questions

**Q: KillAura is not hitting players**  
A: Make sure you have loaded an appropriate config for the server you are playing on (`.config list` and `.config load <name>`). Many module settings need to be tuned per-server to work correctly. Also check that the module is actually enabled (highlighted in the ClickGUI).

**Q: KillAura freezes me in place**  
A: This can happen if the rotation settings conflict with your movement. Try loading a server-specific config using `.config load <name>`, which will have properly tuned settings.

**Q: KillAura attacks too fast (spam clicking)**  
A: Right-click **KillAura** in the ClickGUI to open its settings and adjust the **CPS** (clicks per second) range. Loading a server-specific config with `.config load <name>` will set appropriate attack speeds for that server's anti-cheat.

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Clicker (Setting Group)
│   ├── CPS (Integer Range | default: 5..8 | range: 1..60 | clicks)
│   ├── Technique (Choice | default: STABILIZED | options: Stabilized, Efficient, Spamming, DoubleClick, Drag, Butterfly, NormalDistribution)
│   ├── ItemCooldown (Setting Group)
│   │   ├── Minimum (Decimal Range | default: 1.0..1.0 | range: 0.0..2.0)
│   │   ├── IgnoreOnShieldBreak (Toggle | default: true)
│   │   ├── IgnoreOnMaceSmash (Toggle | default: true)
│   │   └── IgnoreWhenExitingRange (Toggle | default: true)
│   └── AttackCooldown (Toggle | default: true)
├── Range (Setting Group)
│   ├── RangeIncrease (Decimal | default: 1.0 | range: 0.0..5.0 | blocks)
│   ├── ThroughWallsRange (Decimal | default: 3.0 | range: 0.0..8.0 | blocks)
│   └── ScanRangeIncrease (Decimal Range | default: 2.0..3.0 | range: 0.0..7.0 | blocks)
├── Target (Setting Group)
│   ├── FOV (Decimal | default: 180.0 | range: 0.0..180.0)
│   ├── HurtTime (Integer | default: 10 | range: 0..10)
│   ├── Priority (Multi-Select | default: [Type, Health] | options: Type, Health, Distance, Direction, HurtTime, Age)
│   └── IgnoreShield (Toggle | default: true)
├── Rotations (Setting Group)
│   ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Interpolation, Acceleration, AI)
│   │   ├── [Mode: Linear]
│   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   ├── [Mode: Sigmoid]
│   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   ├── [Mode: Interpolation]
│   │   │   ├── HorizontalSpeed (Integer Range | default: 80..85 | range: 1..100 | %)
│   │   │   ├── VerticalSpeed (Integer Range | default: 20..25 | range: 1..100 | %)
│   │   │   ├── DirectionChangeFactor (Integer Range | default: 95..100 | range: 0..100 | %)
│   │   │   └── Midpoint (Decimal | default: 0.35 | range: 0.0..1.0)
│   │   ├── [Mode: Acceleration]
│   │   │   ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │   ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │   ├── DynamicAccel (Toggleable Group | default: off)
│   │   │   │   ├── Enabled (Toggle | default: false)
│   │   │   │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│   │   │   │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │   │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │   ├── AccelerationError (Toggleable Group | default: on)
│   │   │   │   ├── Enabled (Toggle | default: true)
│   │   │   │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   ├── ConstantError (Toggleable Group | default: on)
│   │   │   │   ├── Enabled (Toggle | default: true)
│   │   │   │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   └── SigmoidDeceleration (Toggleable Group | default: off)
│   │   │       ├── Enabled (Toggle | default: false)
│   │   │       ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │       └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   └── [Mode: AI]
│   │       ├── Model (Mode Selector | default: 21KC11KP | modes: 21KC11KP, 19KC8KP)
│   │       ├── Correction (Mode Selector | default: Interpolation | modes: Interpolation, Linear, None)
│   │       │   ├── [Mode: Interpolation]
│   │       │   │   ├── HorizontalSpeed (Integer Range | default: 2..5 | range: 1..100 | %)
│   │       │   │   ├── VerticalSpeed (Integer Range | default: 2..5 | range: 1..100 | %)
│   │       │   │   ├── DirectionChangeFactor (Integer Range | default: 95..100 | range: 0..100 | %)
│   │       │   │   └── Midpoint (Decimal | default: 0.35 | range: 0.0..1.0)
│   │       │   ├── [Mode: Linear]
│   │       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 5.0..5.0 | range: 0.0..180.0)
│   │       │   │   └── VerticalTurnSpeed (Decimal Range | default: 5.0..5.0 | range: 0.0..180.0)
│   │       └── OutputMultiplier (Setting Group)
│   │           ├── Yaw (Decimal | default: 1.5 | range: 0.5..2.0)
│   │           └── Pitch (Decimal | default: 1.0 | range: 0.5..2.0)
│   ├── ShortStop (Toggleable Group | default: off)
│   │   ├── Enabled (Toggle | default: false)
│   │   ├── Rate (Integer | default: 3 | range: 1..25 | %)
│   │   └── Duration (Integer Range | default: 1..2 | range: 1..5 | ticks)
│   ├── Fail (Toggleable Group | default: off)
│   │   ├── Enabled (Toggle | default: false)
│   │   ├── Rate (Integer | default: 3 | range: 1..100 | %)
│   │   ├── Factor (Decimal | default: 0.04 | range: 0.01..0.99)
│   │   ├── StrengthHorizontal (Decimal Range | default: 5.0..10.0 | range: 1.0..90.0 | °)
│   │   ├── StrengthVertical (Decimal Range | default: 0.0..2.0 | range: 0.0..90.0 | °)
│   │   └── TransitionInDuration (Integer Range | default: 1..4 | range: 0..20 | ticks)
│   ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│   ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│   ├── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│   ├── RotationTiming (Choice | default: NORMAL | options: Normal, Snap, OnTick)
│   └── ThroughWalls (Toggle | default: false)
├── AimPoint (Setting Group)
│   ├── ExemptBoxParts (Multi-Select | options: Head, Body, Feet)
│   ├── ExemptBestHitVector (Toggleable Group | default: off)
│   │   ├── Enabled (Toggle | default: false)
│   │   ├── Vertical (Decimal | default: 0.2 | range: 0.0..1.0)
│   │   └── Horizontal (Decimal | default: 0.1 | range: 0.0..1.0)
│   ├── Gaussian (Toggleable Group | default: off)
│   │   ├── Enabled (Toggle | default: false)
│   │   ├── YawOffset (Decimal Range | default: 0.0..0.0 | range: 0.0..1.0)
│   │   ├── PitchOffset (Decimal Range | default: 0.0..0.0 | range: 0.0..1.0)
│   │   ├── Chance (Integer | default: 100 | range: 0..100 | %)
│   │   ├── Speed (Decimal Range | default: 0.1..0.2 | range: 0.01..1.0)
│   │   ├── Tolerance (Decimal | default: 0.05 | range: 0.01..0.1)
│   │   └── Dynamic (Toggleable Group | default: off)
│   │       ├── Enabled (Toggle | default: false)
│   │       ├── HurtTime (Integer | default: 10 | range: 0..10)
│   │       ├── YawFactor (Decimal | default: 0.0 | range: 0.0..10.0 | x)
│   │       ├── PitchFactor (Decimal | default: 0.0 | range: 0.0..10.0 | x)
│   │       ├── Speed (Decimal Range | default: 0.5..0.75 | range: 0.01..1.0)
│   │       └── Tolerance (Decimal | default: 0.1 | range: 0.01..0.1)
│   ├── Lazy (Toggleable Group | default: off)
│   │   ├── Enabled (Toggle | default: false)
│   │   └── Threshold (Decimal Range | default: 0.1..0.2 | range: 0.01..0.4 | m)
│   └── Delay (Toggleable Group | default: off)
│       ├── Enabled (Toggle | default: false)
│       └── Delay (Integer Range | default: 2..4 | range: 0..5 | ticks)
├── Requires (Multi-Select | options: Click, Weapon, VanillaName, NotBreaking)
├── Raycast (Choice | default: TRACE_ALL | options: None, Enemy, All)
├── Criticals (Choice | default: SMART | options: Smart, Ignore, Always)
├── KeepSprint (Toggle | default: true)
├── IgnoreOpenInventory (Toggle | default: true)
├── SimulateInventoryClosing (Toggle | default: true)
├── AutoBlocking (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── BlockMode (Choice | default: INTERACT | options: Basic, Interact, Hypixel, Fake)
│   ├── UnblockMode (Choice | default: STOP_USING_ITEM | options: StopUsingItem, ChangeSlot, SwapHand, None)
│   ├── TickOff (Integer Range | default: 0..0 | range: 0..5 | ticks)
│   ├── TickOn (Integer Range | default: 0..0 | range: 0..5 | ticks)
│   ├── Chance (Decimal | default: 100.0 | range: 0.0..100.0 | %)
│   ├── Blink (Integer | default: 0 | range: 0..10 | ticks)
│   ├── OnScanRange (Toggle | default: true)
│   └── OnlyWhenInDanger (Toggle | default: false)
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
├── FailSwing (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── AdditionalRange (Decimal Range | default: 2.5..3.0 | range: 0.0..10.0)
│   └── NotifyWhenFail (Mode Selector | default: Box | modes: None, Box, Sound)
│       ├── [Mode: Box]
│       │   ├── Fade (Integer | default: 4 | range: 1..10 | secs)
│       │   ├── Color (Color)
│       │   └── Rainbow (Toggle | default: false)
│       └── [Mode: Sound]
│           ├── Volume (Decimal | default: 50.0 | range: 0.0..100.0)
│           └── Pitch (Decimal | default: 0.8 | range: 0.0..2.0)
├── FightBot (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── Auto (Multi-Select | default: [Jump, Swim, Sprint] | options: Jump, Swim, Sprint)
│   ├── OpponentRange (Decimal | default: 3.0 | range: 0.1..10.0)
│   ├── DangerousYaw (Decimal | default: 55.0 | range: 0.0..90.0 | °)
│   ├── RunawayOnCooldown (Toggle | default: true)
│   ├── TargetFilter (Setting Group)
│   │   ├── Range (Decimal | default: 50.0 | range: 10.0..100.0)
│   │   ├── VisibleOnly (Toggle | default: true)
│   │   └── NotWhenVoid (Toggle | default: true)
│   └── Leader (Toggleable Group | default: off)
│       ├── Enabled (Toggle | default: false)
│       ├── Username (Text)
│       └── Radius (Decimal | default: 5.0 | range: 2.0..10.0)
└── RangeIndicator (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── ColorMode (Choice | default: STATIC | options: Static, Rainbow, Distance)
    ├── IdleColor (Color)
    ├── ActiveColor (Color)
    ├── Outline (Toggle | default: true)
    ├── OutlineColor (Color)
    ├── PulseAnimation (Toggle | default: false)
    ├── PulseSpeed (Decimal | default: 2.0 | range: 0.5..5.0)
    ├── PulseIntensity (Decimal | default: 0.15 | range: 0.05..0.5)
    ├── FadeAnimation (Toggle | default: true)
    ├── FadeSpeed (Decimal | default: 0.1 | range: 0.01..0.5)
    ├── WallRangeColor (Color)
    ├── ScanRangeColor (Color)
    ├── OpponentRangeColor (Color)
    ├── HideWhenDead (Toggle | default: true)
    ├── HideWhenSpectator (Toggle | default: true)
    ├── HideInVehicle (Toggle | default: false)
    ├── RespectInventorySetting (Toggle | default: true)
    └── CanBeCovered (Toggle | default: false)
```

### Settings Details

#### Clicker

> For details on Clicker settings, see [Shared: Clicker](/docs/modules/shared/clicker).

##### ItemCooldown

A group of related settings.

- **Minimum** (Decimal Range) — default: `1.0` – `1.0`; range: `0.0` – `2.0` — Minimum attack cooldown multiplier required before attacking.
- **IgnoreOnShieldBreak** (Toggle) — default: `true` — Skips cooldown when breaking an enemy's shield.
- **IgnoreOnMaceSmash** (Toggle) — default: `true` — Skips cooldown during mace smash attacks.
- **IgnoreWhenExitingRange** (Toggle) — default: `true` — Skips cooldown if the target is leaving attack range.

- **AttackCooldown** (Toggle) — default: `true` — Waits for the vanilla attack cooldown before attacking.

#### Range

A group of related settings.

- **RangeIncrease** (Decimal) — default: `1.0`; range: `0.0` – `5.0`; unit: blocks — Additional attack range added beyond the vanilla reach distance.
- **ThroughWallsRange** (Decimal) — default: `3.0`; range: `0.0` – `8.0`; unit: blocks — Maximum distance to attack targets through walls.
- **ScanRangeIncrease** (Decimal Range) — default: `2.0` – `3.0`; range: `0.0` – `7.0`; unit: blocks — Extra range for scanning and tracking targets beyond attack range.

#### Target

> For details on Target settings, see [Shared: Target](/docs/modules/shared/target).

- **FOV** (Decimal) — default: `180.0`; range: `0.0` – `180.0`
- **HurtTime** (Integer) — default: `10`; range: `0` – `10`
- **Priority** (Multi-Select) — default: `Type`, `Health`; options: `Type`, `Health`, `Distance`, `Direction`, `HurtTime`, `Age`
- **IgnoreShield** (Toggle) — default: `true` — Allows attacking players who are blocking with a shield.

#### Rotations

> For details on Rotations settings, see [Shared: Rotations](/docs/modules/shared/rotations).

##### AngleSmooth

Select a mode for this feature. Available modes: **Linear**, **Sigmoid**, **Interpolation**, **Acceleration**, **AI**. Default: **Linear**.

###### Mode: Linear

- **HorizontalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **VerticalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`

###### Mode: Sigmoid

- **HorizontalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **VerticalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **Steepness** (Decimal) — default: `10.0`; range: `0.0` – `20.0`
- **Midpoint** (Decimal) — default: `0.3`; range: `0.0` – `1.0`

###### Mode: Interpolation

- **HorizontalSpeed** (Integer Range) — default: `80` – `85`; range: `1` – `100`; unit: %
- **VerticalSpeed** (Integer Range) — default: `20` – `25`; range: `1` – `100`; unit: %
- **DirectionChangeFactor** (Integer Range) — default: `95` – `100`; range: `0` – `100`; unit: %
- **Midpoint** (Decimal) — default: `0.35`; range: `0.0` – `1.0`

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


###### Mode: AI

###### Model

Select a mode for this feature. Available modes: **21KC11KP**, **19KC8KP**. Default: **21KC11KP**.

###### Correction

Select a mode for this feature. Available modes: **Interpolation**, **Linear**, **None**. Default: **Interpolation**.

###### Mode: Interpolation

- **HorizontalSpeed** (Integer Range) — default: `2` – `5`; range: `1` – `100`; unit: %
- **VerticalSpeed** (Integer Range) — default: `2` – `5`; range: `1` – `100`; unit: %
- **DirectionChangeFactor** (Integer Range) — default: `95` – `100`; range: `0` – `100`; unit: %
- **Midpoint** (Decimal) — default: `0.35`; range: `0.0` – `1.0`

###### Mode: Linear

- **HorizontalTurnSpeed** (Decimal Range) — default: `5.0` – `5.0`; range: `0.0` – `180.0`
- **VerticalTurnSpeed** (Decimal Range) — default: `5.0` – `5.0`; range: `0.0` – `180.0`

###### OutputMultiplier

A group of related settings.

- **Yaw** (Decimal) — default: `1.5`; range: `0.5` – `2.0`
- **Pitch** (Decimal) — default: `1.0`; range: `0.5` – `2.0`


##### ShortStop

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Rate** (Integer) — default: `3`; range: `1` – `25`; unit: % — Chance per tick to briefly stop rotation, simulating human hesitation.
- **Duration** (Integer Range) — default: `1` – `2`; range: `1` – `5`; unit: ticks — How long the rotation pause lasts.

##### Fail

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Rate** (Integer) — default: `3`; range: `1` – `100`; unit: % — Chance per tick to intentionally miss the rotation target.
- **Factor** (Decimal) — default: `0.04`; range: `0.01` – `0.99` — Controls how much the fail rotation deviates from the target.
- **StrengthHorizontal** (Decimal Range) — default: `5.0` – `10.0`; range: `1.0` – `90.0`; unit: ° — Maximum horizontal angle offset when a fail occurs.
- **StrengthVertical** (Decimal Range) — default: `0.0` – `2.0`; range: `0.0` – `90.0`; unit: ° — Maximum vertical angle offset when a fail occurs.
- **TransitionInDuration** (Integer Range) — default: `1` – `4`; range: `0` – `20`; unit: ticks — Ticks to smoothly transition into the fail rotation.

- **RotationTiming** (Choice) — default: `NORMAL`; options: `Normal`, `Snap`, `OnTick` — Controls when rotations are applied: normally, snapped instantly, or on tick.
- **ThroughWalls** (Toggle) — default: `false` — Allows aiming at targets through walls.

#### AimPoint

> For details on AimPoint settings, see [Shared: AimPoint](/docs/modules/shared/aim-point).

- **Requires** (Multi-Select) — options: `Click`, `Weapon`, `VanillaName`, `NotBreaking` — Conditions that must be met before KillAura attacks.
- **Raycast** (Choice) — default: `TRACE_ALL`; options: `None`, `Enemy`, `All` — Determines raycast filtering mode: none, enemies only, or all entities.
- **Criticals** (Choice) — default: `SMART`; options: `Smart`, `Ignore`, `Always` — Controls when to wait for critical hit opportunities before attacking.
- **KeepSprint** (Toggle) — default: `true` — Maintains sprint state during attacks instead of slowing down.
- **IgnoreOpenInventory** (Toggle) — default: `true` — Allows attacking while the inventory screen is open.
- **SimulateInventoryClosing** (Toggle) — default: `true` — Sends inventory close packets before attacking when inventory is open.
#### AutoBlocking

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **BlockMode** (Choice) — default: `INTERACT`; options: `Basic`, `Interact`, `Hypixel`, `Fake` — Method used to activate shield blocking.
- **UnblockMode** (Choice) — default: `STOP_USING_ITEM`; options: `StopUsingItem`, `ChangeSlot`, `SwapHand`, `None` — Method used to stop blocking before attacking.
- **TickOff** (Integer Range) — default: `0` – `0`; range: `0` – `5`; unit: ticks — Ticks to stay unblocked before attacking.
- **TickOn** (Integer Range) — default: `0` – `0`; range: `0` – `5`; unit: ticks — Ticks to wait before re-blocking after attacking.
- **Chance** (Decimal) — default: `100.0`; range: `0.0` – `100.0`; unit: % — Probability of auto-blocking per attack cycle.
- **Blink** (Integer) — default: `0`; range: `0` – `10`; unit: ticks — Ticks to delay packets while blocking for anti-cheat bypass.
- **OnScanRange** (Toggle) — default: `true` — Starts blocking when a target is within scan range, not just attack range.
- **OnlyWhenInDanger** (Toggle) — default: `false` — Only blocks when the player is in danger of being hit.

#### TargetRendering

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


#### FailSwing

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **AdditionalRange** (Decimal Range) — default: `2.5` – `3.0`; range: `0.0` – `10.0` — Extra range beyond attack range to swing at air when no target is hit.
##### NotifyWhenFail

Select a mode for this feature. Available modes: **None**, **Box**, **Sound**. Default: **Box**.

###### Mode: Box

- **Fade** (Integer) — default: `4`; range: `1` – `10`; unit: secs
- **Color** (Color)
- **Rainbow** (Toggle) — default: `false`

###### Mode: Sound

- **Volume** (Decimal) — default: `50.0`; range: `0.0` – `100.0`
- **Pitch** (Decimal) — default: `0.8`; range: `0.0` – `2.0`


#### FightBot

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Auto** (Multi-Select) — default: `Jump`, `Swim`, `Sprint`; options: `Jump`, `Swim`, `Sprint` — Automated movement actions during combat.
- **OpponentRange** (Decimal) — default: `3.0`; range: `0.1` – `10.0` — Preferred distance to maintain from the opponent.
- **DangerousYaw** (Decimal) — default: `55.0`; range: `0.0` – `90.0`; unit: ° — Yaw angle threshold to determine when the opponent faces a dangerous direction.
- **RunawayOnCooldown** (Toggle) — default: `true` — Moves away from the opponent while attack cooldown is active.
##### TargetFilter

A group of related settings.

- **Range** (Decimal) — default: `50.0`; range: `10.0` – `100.0` — Maximum range to search for fight targets.
- **VisibleOnly** (Toggle) — default: `true` — Only targets enemies that are visible (line-of-sight).
- **NotWhenVoid** (Toggle) — default: `true` — Prevents fighting when the player is near the void.

##### Leader

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Username** (Text) — Username of the leader player to follow.
- **Radius** (Decimal) — default: `5.0`; range: `2.0` – `10.0` — Distance to stay within from the leader player.


#### RangeIndicator

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **ColorMode** (Choice) — default: `STATIC`; options: `Static`, `Rainbow`, `Distance` — Color mode for the range indicator circle.
- **IdleColor** (Color) — Color when no target is in range.
- **ActiveColor** (Color) — Color when a target is within attack range.
- **Outline** (Toggle) — default: `true` — Draws an outline around the range indicator.
- **OutlineColor** (Color) — Color of the range indicator outline.
- **PulseAnimation** (Toggle) — default: `false` — Enables a pulsing animation effect on the indicator.
- **PulseSpeed** (Decimal) — default: `2.0`; range: `0.5` – `5.0` — Speed of the pulse animation.
- **PulseIntensity** (Decimal) — default: `0.15`; range: `0.05` – `0.5` — Intensity of the pulse animation.
- **FadeAnimation** (Toggle) — default: `true` — Enables a smooth fade animation when the indicator appears or disappears.
- **FadeSpeed** (Decimal) — default: `0.1`; range: `0.01` – `0.5` — Speed of the fade animation.
- **WallRangeColor** (Color) — Color indicating the through-walls attack range.
- **ScanRangeColor** (Color) — Color indicating the scan range area.
- **OpponentRangeColor** (Color) — Color indicating the opponent's attack range.
- **HideWhenDead** (Toggle) — default: `true` — Hides the indicator when the player is dead.
- **HideWhenSpectator** (Toggle) — default: `true` — Hides the indicator when in spectator mode.
- **HideInVehicle** (Toggle) — default: `false` — Hides the indicator when riding a vehicle.
- **RespectInventorySetting** (Toggle) — default: `true` — Hides the indicator when inventory is open, respecting the IgnoreOpenInventory setting.
- **CanBeCovered** (Toggle) — default: `false` — Allows the indicator to be covered by other rendered objects.


### Screenshots

*Screenshots for KillAura will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleKillAura.kt)*
