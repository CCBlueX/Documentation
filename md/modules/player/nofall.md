## NoFall

Protects you from taking fall damage.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: SpoofGround | modes: SpoofGround, SpoofLanding, NoGround, Packet, PacketJump, MLG, Rettungsplatform, Spartan524Flag, Vulcan277, VulcanTP288, Verus, ForceJump, Cancel, Blink, HypixelPacket, Hypixel, BlocksMC, Grim2371-1.9+)
│   ├── [Mode: SpoofGround]
│   │   ├── FallDistance (Mode Selector | default: Smart | modes: Smart, Constant)
│   │   │   └── [Mode: Constant]
│   │   │       └── Value (Decimal | default: 1.7 | range: 0.0..5.0)
│   │   └── ResetFallDistance (Toggle | default: true)
│   ├── [Mode: SpoofLanding]
│   │   └── Modification (3D Position)
│   ├── [Mode: Packet]
│   │   ├── PacketType (Choice | default: FULL | options: OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full)
│   │   └── Filter (Mode Selector | default: FallDistance | modes: FallDistance, Always)
│   │       ├── [Mode: FallDistance]
│   │       │   ├── Distance (Mode Selector | default: Smart | modes: Smart, Constant)
│   │       │   │   └── [Mode: Constant]
│   │       │   │       └── Value (Decimal | default: 2.0 | range: 0.0..5.0)
│   │       │   └── ResetFallDistance (Toggle | default: true)
│   ├── [Mode: PacketJump]
│   │   ├── PacketType (Choice | default: FULL | options: PositionAndOnGround, Full)
│   │   ├── FallDistance (Mode Selector | default: Smart | modes: Smart, Constant)
│   │   │   └── [Mode: Constant]
│   │   │       └── Value (Decimal | default: 3.0 | range: 0.0..5.0)
│   │   └── Timing (Mode Selector | default: Landing | modes: Landing, Falling)
│   │       └── [Mode: Falling]
│   │           └── ResetFallDistance (Toggle | default: true)
│   ├── [Mode: MLG]
│   │   ├── MinFallDistance (Decimal | default: 5.0 | range: 2.0..50.0)
│   │   ├── Rotations (Setting Group)
│   │   │   ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│   │   │   │   ├── [Mode: Linear]
│   │   │   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │   ├── [Mode: Sigmoid]
│   │   │   │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │   │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   │   │   └── [Mode: Acceleration]
│   │   │   │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │   │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │   │       ├── DynamicAccel (Toggleable Group | default: off)
│   │   │   │       │   ├── Enabled (Toggle | default: false)
│   │   │   │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│   │   │   │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │   │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │   │       ├── AccelerationError (Toggleable Group | default: on)
│   │   │   │       │   ├── Enabled (Toggle | default: true)
│   │   │   │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       ├── ConstantError (Toggleable Group | default: on)
│   │   │   │       │   ├── Enabled (Toggle | default: true)
│   │   │   │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       └── SigmoidDeceleration (Toggleable Group | default: off)
│   │   │   │           ├── Enabled (Toggle | default: false)
│   │   │   │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │   │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   │   ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│   │   │   ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│   │   │   └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│   │   └── PickUpWater (Toggleable Group | default: on)
│   │       ├── Enabled (Toggle | default: true)
│   │       └── PickupSpan (Integer Range | default: 200..1000 | range: 0..10000 | ms)
│   ├── [Mode: VulcanTP288]
│   │   └── VoidLevel (Integer | default: 0 | range: -256..0)
│   ├── [Mode: ForceJump]
│   │   ├── BlockDistance (Decimal | default: 1.0 | range: 0.1..5.0)
│   │   ├── FallDistance (Decimal | default: 3.35 | range: 3.35..10.0)
│   │   └── JumpHeight (Decimal | default: 0.42 | range: 0.1..0.42)
│   ├── [Mode: Cancel]
│   │   ├── FallDistance (Mode Selector | default: Smart | modes: Smart, Constant)
│   │   │   └── [Mode: Constant]
│   │   │       └── Value (Decimal | default: 1.7 | range: 0.0..5.0)
│   │   ├── ResetFallDistance (Toggle | default: true)
│   │   └── CancelSetbackPacket (Toggle | default: false)
│   ├── [Mode: Blink]
│   │   ├── TriggerFallDistance (Decimal | default: 2.5 | range: 0.5..3.0)
│   │   └── MaximumFallDistance (Decimal | default: 20.0 | range: 2.0..50.0)
│   ├── [Mode: HypixelPacket]
│   │   └── OverVoid (Toggle | default: false)
└── Not (Multi-Select | options: WhileGliding, WithMace)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **SpoofGround**, **SpoofLanding**, **NoGround**, **Packet**, **PacketJump**, **MLG**, **Rettungsplatform**, **Spartan524Flag**, **Vulcan277**, **VulcanTP288**, **Verus**, **ForceJump**, **Cancel**, **Blink**, **HypixelPacket**, **Hypixel**, **BlocksMC**, **Grim2371-1.9+**. Default: **SpoofGround**.

##### Mode: SpoofGround

###### FallDistance

Select a mode for this feature. Available modes: **Smart**, **Constant**. Default: **Smart**.

###### Mode: Constant

- **Value** (Decimal) — default: `1.7`; range: `0.0` – `5.0`

- **ResetFallDistance** (Toggle) — default: `true`

##### Mode: SpoofLanding

- **Modification** (3D Position)

##### Mode: Packet

- **PacketType** (Choice) — default: `FULL`; options: `OnGroundOnly`, `PositionAndOnGround`, `LookAndOnGround`, `Full`
###### Filter

Select a mode for this feature. Available modes: **FallDistance**, **Always**. Default: **FallDistance**.

###### Mode: FallDistance

###### Distance

Select a mode for this feature. Available modes: **Smart**, **Constant**. Default: **Smart**.

###### Mode: Constant

- **Value** (Decimal) — default: `2.0`; range: `0.0` – `5.0`

- **ResetFallDistance** (Toggle) — default: `true`


##### Mode: PacketJump

- **PacketType** (Choice) — default: `FULL`; options: `PositionAndOnGround`, `Full`
###### FallDistance

Select a mode for this feature. Available modes: **Smart**, **Constant**. Default: **Smart**.

###### Mode: Constant

- **Value** (Decimal) — default: `3.0`; range: `0.0` – `5.0`

###### Timing

Select a mode for this feature. Available modes: **Landing**, **Falling**. Default: **Landing**.

###### Mode: Falling

- **ResetFallDistance** (Toggle) — default: `true`


##### Mode: MLG

- **MinFallDistance** (Decimal) — default: `5.0`; range: `2.0` – `50.0`
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

###### PickUpWater

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **PickupSpan** (Integer Range) — default: `200` – `1000`; range: `0` – `10000`; unit: ms


##### Mode: VulcanTP288

- **VoidLevel** (Integer) — default: `0`; range: `-256` – `0`

##### Mode: ForceJump

- **BlockDistance** (Decimal) — default: `1.0`; range: `0.1` – `5.0`
- **FallDistance** (Decimal) — default: `3.35`; range: `3.35` – `10.0`
- **JumpHeight** (Decimal) — default: `0.42`; range: `0.1` – `0.42`

##### Mode: Cancel

###### FallDistance

Select a mode for this feature. Available modes: **Smart**, **Constant**. Default: **Smart**.

###### Mode: Constant

- **Value** (Decimal) — default: `1.7`; range: `0.0` – `5.0`

- **ResetFallDistance** (Toggle) — default: `true`
- **CancelSetbackPacket** (Toggle) — default: `false`

##### Mode: Blink

- **TriggerFallDistance** (Decimal) — default: `2.5`; range: `0.5` – `3.0`
- **MaximumFallDistance** (Decimal) — default: `20.0`; range: `2.0` – `50.0`

##### Mode: HypixelPacket

- **OverVoid** (Toggle) — default: `false`

- **Not** (Multi-Select) — options: `WhileGliding`, `WithMace`

### Screenshots

*Screenshots for NoFall will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleNoFall.kt)*
