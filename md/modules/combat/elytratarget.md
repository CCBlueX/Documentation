## ElytraTarget

Following the target on elytra.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Target (Setting Group)
│   ├── FOV (Decimal | default: 180.0 | range: 0.0..180.0)
│   ├── HurtTime (Integer | default: 10 | range: 0..10)
│   └── Priority (Multi-Select | default: [Type, Health] | options: Type, Health, Distance, Direction, HurtTime, Age)
├── Rotations (Setting Group)
│   ├── Sharp (Toggle | default: false)
│   ├── IgnoreKillAuraRotation (Toggle | default: true)
│   ├── Look (Toggle | default: false)
│   ├── AutoDistance (Toggle | default: true)
│   ├── Prediction (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   ├── Mode (Choice | default: SIMPLE | options: Simple, WithGravity)
│   │   ├── GlidingOnly (Toggle | default: true)
│   │   └── Multiplier (Decimal Range | default: 1.8..2.0 | range: 0.5..3.0)
│   └── RotateAt (Choice | default: EYES | options: Eyes, Center)
├── AutoFirework (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── UseMode (Choice | default: NORMAL | options: Normal, Packet)
│   ├── ExtraDistance (Decimal | default: 50.0 | range: 5.0..100.0 | m)
│   ├── SlotResetDelay (Integer Range | default: 0..0 | range: 0..20 | ticks)
│   ├── SyncCooldownWithKillAura (Toggle | default: false)
│   └── Cooldown (Integer Range | default: 8..10 | range: 1..50 | ticks)
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
├── Safe (Toggle | default: true)
└── AlwaysGlide (Toggle | default: false)
```

### Settings Details

#### Target

A group of related settings.

- **FOV** (Decimal) — default: `180.0`; range: `0.0` – `180.0`
- **HurtTime** (Integer) — default: `10`; range: `0` – `10`
- **Priority** (Multi-Select) — default: `Type`, `Health`; options: `Type`, `Health`, `Distance`, `Direction`, `HurtTime`, `Age`

#### Rotations

A group of related settings.

- **Sharp** (Toggle) — default: `false`
- **IgnoreKillAuraRotation** (Toggle) — default: `true`
- **Look** (Toggle) — default: `false`
- **AutoDistance** (Toggle) — default: `true`
##### Prediction

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Mode** (Choice) — default: `SIMPLE`; options: `Simple`, `WithGravity`
- **GlidingOnly** (Toggle) — default: `true`
- **Multiplier** (Decimal Range) — default: `1.8` – `2.0`; range: `0.5` – `3.0`

- **RotateAt** (Choice) — default: `EYES`; options: `Eyes`, `Center`

#### AutoFirework

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **UseMode** (Choice) — default: `NORMAL`; options: `Normal`, `Packet`
- **ExtraDistance** (Decimal) — default: `50.0`; range: `5.0` – `100.0`; unit: m
- **SlotResetDelay** (Integer Range) — default: `0` – `0`; range: `0` – `20`; unit: ticks
- **SyncCooldownWithKillAura** (Toggle) — default: `false`
- **Cooldown** (Integer Range) — default: `8` – `10`; range: `1` – `50`; unit: ticks

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


- **Safe** (Toggle) — default: `true`
- **AlwaysGlide** (Toggle) — default: `false`

### Screenshots

*Screenshots for ElytraTarget will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleElytraTarget.kt)*
