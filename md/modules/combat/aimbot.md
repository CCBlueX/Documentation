## Aimbot

Automatically faces targets nearby.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Range (Decimal | default: 4.2 | range: 1.0..8.0)
├── Target (Setting Group)
│   ├── FOV (Decimal | default: 180.0 | range: 0.0..180.0)
│   ├── HurtTime (Integer | default: 10 | range: 0..10)
│   └── Priority (Multi-Select | default: [Type, Direction] | options: Type, Health, Distance, Direction, HurtTime, Age)
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
├── AngleSmooth (Mode Selector | default: Interpolation | modes: Interpolation, Sigmoid, Linear)
│   ├── [Mode: Interpolation]
│   │   ├── HorizontalSpeed (Integer Range | default: 80..85 | range: 1..100 | %)
│   │   ├── VerticalSpeed (Integer Range | default: 20..25 | range: 1..100 | %)
│   │   ├── DirectionChangeFactor (Integer Range | default: 95..100 | range: 0..100 | %)
│   │   └── Midpoint (Decimal | default: 0.35 | range: 0.0..1.0)
│   ├── [Mode: Sigmoid]
│   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   └── [Mode: Linear]
│       ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│       └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
└── Ignore (Multi-Select | options: Screen, Container)
```

### Settings Details

- **Range** (Decimal) — default: `4.2`; range: `1.0` – `8.0` — Maximum distance in blocks at which the module can target entities.
#### Target

> For details on Target settings, see [Shared: Target](/docs/modules/shared/target).

- **FOV** (Decimal) — default: `180.0`; range: `0.0` – `180.0`
- **HurtTime** (Integer) — default: `10`; range: `0` – `10`
- **Priority** (Multi-Select) — default: `Type`, `Direction`; options: `Type`, `Health`, `Distance`, `Direction`, `HurtTime`, `Age`

#### TargetRendering

> For details on TargetRendering settings, see [Shared: TargetRendering](/docs/modules/shared/target-rendering).

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


#### AimPoint

> For details on AimPoint settings, see [Shared: AimPoint](/docs/modules/shared/aim-point).

- **Requires** (Multi-Select) — options: `Click`, `Weapon`, `VanillaName`, `NotBreaking` — Conditions that must be met before the aimbot activates.
#### AngleSmooth

> For details on AngleSmooth settings, see [Shared: Rotations](/docs/modules/shared/rotations).

Select a mode for this feature. Available modes: **Interpolation**, **Sigmoid**, **Linear**. Default: **Interpolation**.

##### Mode: Interpolation

- **HorizontalSpeed** (Integer Range) — default: `80` – `85`; range: `1` – `100`; unit: %
- **VerticalSpeed** (Integer Range) — default: `20` – `25`; range: `1` – `100`; unit: %
- **DirectionChangeFactor** (Integer Range) — default: `95` – `100`; range: `0` – `100`; unit: %
- **Midpoint** (Decimal) — default: `0.35`; range: `0.0` – `1.0`

##### Mode: Sigmoid

- **HorizontalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **VerticalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **Steepness** (Decimal) — default: `10.0`; range: `0.0` – `20.0`
- **Midpoint** (Decimal) — default: `0.3`; range: `0.0` – `1.0`

##### Mode: Linear

- **HorizontalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`
- **VerticalTurnSpeed** (Decimal Range) — default: `180.0` – `180.0`; range: `0.0` – `180.0`

- **Ignore** (Multi-Select) — options: `Screen`, `Container` — Prevents aiming when specific screens or containers are open.

### Screenshots

*Screenshots for Aimbot will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleAimbot.kt)*
