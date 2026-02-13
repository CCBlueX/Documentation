## Fly

Allows you to fly in survival mode.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Vanilla | modes: Vanilla, Creative, Jetpack, Enderpearl, AirWalk, Explosion, Fireball, Vulcan277, Vulcan286-113, Vulcan286-18, Vulcan286-Teleport-18, Grim2859-V, Grim2373Jan15, Spartan524, Sentinel20thApr, Sentinel27thJan, Sentinel10thMar, Sentinel26thDec, VerusB3896Damage, VerusB3896Flat, NcpClip, Hypixel, HypixelFlat, HycraftDamage)
│   ├── [Mode: Vanilla]
│   │   ├── Glide (Decimal | default: 0.0 | range: -1.0..1.0)
│   │   ├── BypassVanillaCheck (Toggle | default: true)
│   │   ├── BaseSpeed (Setting Group)
│   │   │   ├── Horizontal (Decimal | default: 0.44 | range: 0.1..10.0)
│   │   │   └── Vertical (Decimal | default: 0.44 | range: 0.1..10.0)
│   │   └── SprintSpeed (Toggleable Group | default: on)
│   │       ├── Enabled (Toggle | default: true)
│   │       ├── Horizontal (Decimal | default: 1.0 | range: 0.1..10.0)
│   │       └── Vertical (Decimal | default: 1.0 | range: 0.1..10.0)
│   ├── [Mode: Creative]
│   │   ├── Speed (Decimal | default: 0.1 | range: 0.1..5.0)
│   │   ├── SprintSpeed (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── Speed (Decimal | default: 0.1 | range: 0.1..5.0)
│   │   ├── MaxVelocity (Decimal | default: 4.0 | range: 1.0..20.0)
│   │   ├── BypassVanillaCheck (Toggle | default: true)
│   │   └── ForceFlight (Toggle | default: true)
│   ├── [Mode: Enderpearl]
│   │   ├── Speed (Decimal | default: 1.0 | range: 0.5..2.0)
│   │   └── Rotations (Setting Group)
│   │       ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│   │       │   ├── [Mode: Linear]
│   │       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │       │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │       │   ├── [Mode: Sigmoid]
│   │       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │       │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │       │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │       │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │       │   └── [Mode: Acceleration]
│   │       │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │       │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │       │       ├── DynamicAccel (Toggleable Group | default: off)
│   │       │       │   ├── Enabled (Toggle | default: false)
│   │       │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│   │       │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │       │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │       │       ├── AccelerationError (Toggleable Group | default: on)
│   │       │       │   ├── Enabled (Toggle | default: true)
│   │       │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       │       ├── ConstantError (Toggleable Group | default: on)
│   │       │       │   ├── Enabled (Toggle | default: true)
│   │       │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │       │       └── SigmoidDeceleration (Toggleable Group | default: off)
│   │       │           ├── Enabled (Toggle | default: false)
│   │       │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │       │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │       ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│   │       ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│   │       └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│   ├── [Mode: AirWalk]
│   │   └── OnGround (Toggle | default: true)
│   ├── [Mode: Explosion]
│   │   ├── Vertical (Decimal | default: 4.0 | range: 0.0..10.0)
│   │   ├── StartStrafe (Decimal | default: 1.0 | range: 0.6..4.0)
│   │   └── StrafeDecrease (Decimal | default: 0.005 | range: 0.001..0.1)
│   ├── [Mode: Fireball]
│   │   ├── Technique (Mode Selector | default: Legit | modes: Legit, Custom)
│   │   │   ├── [Mode: Legit]
│   │   │   │   ├── Sprint (Toggle | default: true)
│   │   │   │   ├── StopMove (Toggle | default: true)
│   │   │   │   ├── Jump (Toggleable Group | default: on)
│   │   │   │   │   ├── Enabled (Toggle | default: true)
│   │   │   │   │   └── Delay (Integer | default: 3 | range: 0..20 | ticks)
│   │   │   │   └── Rotations (Setting Group)
│   │   │   │       ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│   │   │   │       │   ├── [Mode: Linear]
│   │   │   │       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │       │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │       │   ├── [Mode: Sigmoid]
│   │   │   │       │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │       │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │   │       │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │   │       │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   │   │       │   └── [Mode: Acceleration]
│   │   │   │       │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │   │       │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │   │       │       ├── DynamicAccel (Toggleable Group | default: off)
│   │   │   │       │       │   ├── Enabled (Toggle | default: false)
│   │   │   │       │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│   │   │   │       │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │   │       │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │   │       │       ├── AccelerationError (Toggleable Group | default: on)
│   │   │   │       │       │   ├── Enabled (Toggle | default: true)
│   │   │   │       │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       │       ├── ConstantError (Toggleable Group | default: on)
│   │   │   │       │       │   ├── Enabled (Toggle | default: true)
│   │   │   │       │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │   │       │       └── SigmoidDeceleration (Toggleable Group | default: off)
│   │   │   │       │           ├── Enabled (Toggle | default: false)
│   │   │   │       │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │   │       │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   │   │       ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│   │   │   │       ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│   │   │   │       ├── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│   │   │   │       ├── Pitch (Decimal | default: 90.0 | range: 0.0..90.0)
│   │   │   │       └── Backwards (Toggle | default: true)
│   │   │   └── [Mode: Custom]
│   │   │       ├── DisableDelay (Integer | default: 10 | range: 0..20)
│   │   │       ├── ThrowDelay (Integer | default: 2 | range: 0..20)
│   │   │       ├── Sprint (Toggle | default: true)
│   │   │       ├── StopMove (Toggle | default: true)
│   │   │       ├── Jump (Toggleable Group | default: on)
│   │   │       │   ├── Enabled (Toggle | default: true)
│   │   │       │   └── JumpDelay (Integer | default: 1 | range: 0..20 | ticks)
│   │   │       ├── YVelocity (Toggleable Group | default: on)
│   │   │       │   ├── Enabled (Toggle | default: true)
│   │   │       │   ├── Velocity (Decimal | default: 0.0 | range: -5.0..5.0)
│   │   │       │   └── Delay (Integer | default: 0 | range: 0..20 | ticks)
│   │   │       └── Rotations (Setting Group)
│   │   │           ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
│   │   │           │   ├── [Mode: Linear]
│   │   │           │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │           │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │           │   ├── [Mode: Sigmoid]
│   │   │           │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │           │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
│   │   │           │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │           │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   │           │   └── [Mode: Acceleration]
│   │   │           │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │           │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
│   │   │           │       ├── DynamicAccel (Toggleable Group | default: off)
│   │   │           │       │   ├── Enabled (Toggle | default: false)
│   │   │           │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
│   │   │           │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │           │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
│   │   │           │       ├── AccelerationError (Toggleable Group | default: on)
│   │   │           │       │   ├── Enabled (Toggle | default: true)
│   │   │           │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │           │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │           │       ├── ConstantError (Toggleable Group | default: on)
│   │   │           │       │   ├── Enabled (Toggle | default: true)
│   │   │           │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │           │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
│   │   │           │       └── SigmoidDeceleration (Toggleable Group | default: off)
│   │   │           │           ├── Enabled (Toggle | default: false)
│   │   │           │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
│   │   │           │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   │           ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
│   │   │           ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
│   │   │           ├── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
│   │   │           └── Pitch (Decimal | default: 90.0 | range: 0.0..90.0)
│   │   ├── Trigger (Mode Selector | default: Instant | modes: Instant, OnEdge)
│   │   │   └── [Mode: OnEdge]
│   │   │       └── EdgeDistance (Decimal | default: 0.01 | range: 0.01..0.5)
│   │   └── SlotResetDelay (Integer Range | default: 4..6 | range: 0..40 | ticks)
│   ├── [Mode: Vulcan286-18]
│   │   ├── Timer (Decimal | default: 2.5 | range: 1.0..2.5)
│   │   └── AutoDisable (Toggle | default: false)
│   ├── [Mode: Grim2859-V]
│   │   ├── Toggle (Integer | default: 0 | range: 0..100)
│   │   └── Timer (Decimal | default: 0.446 | range: 0.1..1.0)
│   ├── [Mode: Grim2373Jan15]
│   │   ├── AutoLagInAir (Toggle | default: true)
│   │   └── AirTick (Integer | default: 3 | range: 0..12 | ticks)
│   ├── [Mode: Sentinel20thApr]
│   │   ├── HorizontalSpeed (Decimal | default: 3.5 | range: 0.1..10.0)
│   │   ├── ConstantSpeed (Toggle | default: false)
│   │   ├── VerticalSpeed (Decimal | default: 0.7 | range: 0.1..1.0)
│   │   ├── ReboostTicks (Integer | default: 30 | range: 10..50)
│   │   ├── BoostOnce (Toggle | default: false)
│   │   └── Nostalgia (Toggle | default: false)
│   ├── [Mode: Sentinel27thJan]
│   │   └── HorizontalSpeed (Decimal Range | default: 0.33..0.34 | range: 0.1..1.0)
│   ├── [Mode: Sentinel10thMar]
│   │   ├── Height (Decimal | default: 0.42 | range: 0.1..1.0)
│   │   ├── Speed (Decimal | default: 0.35 | range: 0.1..1.0)
│   │   └── Ticks (Integer | default: 11 | range: 1..20)
│   ├── [Mode: Sentinel26thDec]
│   │   ├── HorizontalSpeed (Decimal | default: 3.5 | range: 0.1..10.0)
│   │   ├── VerticalSpeed (Decimal | default: 0.7 | range: 0.1..5.0)
│   │   ├── Ticks (Integer | default: 20 | range: 10..50)
│   │   ├── Timer (Decimal | default: 0.5 | range: 0.1..1.0)
│   │   └── Nostalgia (Toggle | default: false)
│   ├── [Mode: VerusB3896Flat]
│   │   └── Timer (Decimal | default: 5.0 | range: 1.0..20.0)
│   ├── [Mode: NcpClip]
│   │   ├── Speed (Decimal | default: 7.5 | range: 2.0..10.0)
│   │   ├── AdditionalEntry (Decimal | default: 2.0 | range: 0.0..2.0)
│   │   ├── Timer (Decimal | default: 0.4 | range: 0.1..1.0)
│   │   ├── Strafe (Toggle | default: true)
│   │   ├── Clipping (Decimal | default: -0.5 | range: -1.0..1.0)
│   │   ├── Blink (Toggle | default: false)
│   │   ├── FallDamage (Toggle | default: false)
│   │   └── MaximumDistance (Decimal | default: 200.0 | range: 0.1..500.0)
│   ├── [Mode: Hypixel]
│   │   └── Timer (Decimal | default: 1.0 | range: 0.1..1.0)
│   ├── [Mode: HypixelFlat]
│   │   ├── Timer (Decimal | default: 1.0 | range: 0.1..1.0)
│   │   └── Speed (Decimal | default: 1.66 | range: 0.8..2.0)
├── Visuals (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Stride (Toggle | default: true)
└── DisableOnSetback (Toggle | default: false)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Vanilla**, **Creative**, **Jetpack**, **Enderpearl**, **AirWalk**, **Explosion**, **Fireball**, **Vulcan277**, **Vulcan286-113**, **Vulcan286-18**, **Vulcan286-Teleport-18**, **Grim2859-V**, **Grim2373Jan15**, **Spartan524**, **Sentinel20thApr**, **Sentinel27thJan**, **Sentinel10thMar**, **Sentinel26thDec**, **VerusB3896Damage**, **VerusB3896Flat**, **NcpClip**, **Hypixel**, **HypixelFlat**, **HycraftDamage**. Default: **Vanilla**.

##### Mode: Vanilla

- **Glide** (Decimal) — default: `0.0`; range: `-1.0` – `1.0` — Vertical velocity when not pressing jump or sneak (negative falls, positive rises).
- **BypassVanillaCheck** (Toggle) — default: `true` — Periodically dips slightly to bypass the vanilla server fly detection.
###### BaseSpeed

A group of related settings.

- **Horizontal** (Decimal) — default: `0.44`; range: `0.1` – `10.0` — Base horizontal flight speed.
- **Vertical** (Decimal) — default: `0.44`; range: `0.1` – `10.0` — Base vertical flight speed.

###### SprintSpeed

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables a separate speed when sprinting.
- **Horizontal** (Decimal) — default: `1.0`; range: `0.1` – `10.0` — Horizontal speed while sprinting.
- **Vertical** (Decimal) — default: `1.0`; range: `0.1` – `10.0` — Vertical speed while sprinting.


##### Mode: Creative

- **Speed** (Decimal) — default: `0.1`; range: `0.1` – `5.0` — Creative flight speed multiplier.
###### SprintSpeed

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables a separate speed when sprinting in creative fly mode.
- **Speed** (Decimal) — default: `0.1`; range: `0.1` – `5.0` — Creative flight speed while sprinting.

- **MaxVelocity** (Decimal) — default: `4.0`; range: `1.0` – `20.0` — Maximum allowed velocity to prevent rubberbanding.
- **BypassVanillaCheck** (Toggle) — default: `true` — Periodically dips slightly to bypass the vanilla server fly detection.
- **ForceFlight** (Toggle) — default: `true` — Forces the player's flight ability to stay enabled.

##### Mode: Enderpearl

- **Speed** (Decimal) — default: `1.0`; range: `0.5` – `2.0` — Flight speed after the enderpearl teleport.
#### Rotations

> For details on Rotations settings, see [Shared: Rotations](/docs/modules/shared/rotations).


##### Mode: AirWalk

- **OnGround** (Toggle) — default: `true` — Spoofs the on-ground state in movement packets.

##### Mode: Explosion

- **Vertical** (Decimal) — default: `4.0`; range: `0.0` – `10.0` — Multiplier for vertical velocity from explosions.
- **StartStrafe** (Decimal) — default: `1.0`; range: `0.6` – `4.0` — Initial horizontal strafe speed after being damaged.
- **StrafeDecrease** (Decimal) — default: `0.005`; range: `0.001` – `0.1` — Amount the strafe speed decreases per tick.

##### Mode: Fireball

###### Technique

Select a mode for this feature. Available modes: **Legit**, **Custom**. Default: **Legit**.

###### Mode: Legit

- **Sprint** (Toggle) — default: `true` — Enables sprinting after throwing the fireball.
- **StopMove** (Toggle) — default: `true` — Stops player movement while preparing the throw to avoid falling off edges.
###### Jump

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables jumping before throwing.
- **Delay** (Integer) — default: `3`; range: `0` – `20`; unit: ticks — Ticks to wait after jumping before throwing.

#### Rotations

> For details on Rotations settings, see [Shared: Rotations](/docs/modules/shared/rotations).

- **Pitch** (Decimal) — default: `90.0`; range: `0.0` – `90.0` — Pitch angle to aim at when throwing the fireball.
- **Backwards** (Toggle) — default: `true` — Rotates the player to face backwards before throwing.


###### Mode: Custom

- **DisableDelay** (Integer) — default: `10`; range: `0` – `20` — Ticks to wait before disabling the module after throwing.
- **ThrowDelay** (Integer) — default: `2`; range: `0` – `20` — Ticks to wait before throwing the fireball.
- **Sprint** (Toggle) — default: `true` — Enables sprinting after throwing the fireball.
- **StopMove** (Toggle) — default: `true` — Stops player movement while preparing the throw to avoid falling off edges.
###### Jump

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables jumping before throwing.
- **JumpDelay** (Integer) — default: `1`; range: `0` – `20`; unit: ticks — Ticks to wait after jumping before throwing.

###### YVelocity

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables setting a custom vertical velocity after throwing.
- **Velocity** (Decimal) — default: `0.0`; range: `-5.0` – `5.0` — Vertical velocity to apply after throwing.
- **Delay** (Integer) — default: `0`; range: `0` – `20`; unit: ticks — Ticks to wait before applying the vertical velocity.

#### Rotations

> For details on Rotations settings, see [Shared: Rotations](/docs/modules/shared/rotations).

- **Pitch** (Decimal) — default: `90.0`; range: `0.0` – `90.0` — Pitch angle to aim at when throwing the fireball.


###### Trigger

Select a mode for this feature. Available modes: **Instant**, **OnEdge**. Default: **Instant**.

###### Mode: OnEdge

- **EdgeDistance** (Decimal) — default: `0.01`; range: `0.01` – `0.5` — How close to the block edge the player must be to trigger the fireball throw.

- **SlotResetDelay** (Integer Range) — default: `4` – `6`; range: `0` – `40`; unit: ticks — Ticks to wait before resetting the hotbar slot after use.

##### Mode: Vulcan286-18

- **Timer** (Decimal) — default: `2.5`; range: `1.0` – `2.5`
- **AutoDisable** (Toggle) — default: `false`

##### Mode: Grim2859-V

- **Toggle** (Integer) — default: `0`; range: `0` – `100`
- **Timer** (Decimal) — default: `0.446`; range: `0.1` – `1.0`

##### Mode: Grim2373Jan15

- **AutoLagInAir** (Toggle) — default: `true`
- **AirTick** (Integer) — default: `3`; range: `0` – `12`; unit: ticks

##### Mode: Sentinel20thApr

- **HorizontalSpeed** (Decimal) — default: `3.5`; range: `0.1` – `10.0`
- **ConstantSpeed** (Toggle) — default: `false`
- **VerticalSpeed** (Decimal) — default: `0.7`; range: `0.1` – `1.0`
- **ReboostTicks** (Integer) — default: `30`; range: `10` – `50`
- **BoostOnce** (Toggle) — default: `false`
- **Nostalgia** (Toggle) — default: `false`

##### Mode: Sentinel27thJan

- **HorizontalSpeed** (Decimal Range) — default: `0.33` – `0.34`; range: `0.1` – `1.0`

##### Mode: Sentinel10thMar

- **Height** (Decimal) — default: `0.42`; range: `0.1` – `1.0`
- **Speed** (Decimal) — default: `0.35`; range: `0.1` – `1.0`
- **Ticks** (Integer) — default: `11`; range: `1` – `20`

##### Mode: Sentinel26thDec

- **HorizontalSpeed** (Decimal) — default: `3.5`; range: `0.1` – `10.0`
- **VerticalSpeed** (Decimal) — default: `0.7`; range: `0.1` – `5.0`
- **Ticks** (Integer) — default: `20`; range: `10` – `50`
- **Timer** (Decimal) — default: `0.5`; range: `0.1` – `1.0`
- **Nostalgia** (Toggle) — default: `false`

##### Mode: VerusB3896Flat

- **Timer** (Decimal) — default: `5.0`; range: `1.0` – `20.0`

##### Mode: NcpClip

- **Speed** (Decimal) — default: `7.5`; range: `2.0` – `10.0`
- **AdditionalEntry** (Decimal) — default: `2.0`; range: `0.0` – `2.0`
- **Timer** (Decimal) — default: `0.4`; range: `0.1` – `1.0`
- **Strafe** (Toggle) — default: `true`
- **Clipping** (Decimal) — default: `-0.5`; range: `-1.0` – `1.0`
- **Blink** (Toggle) — default: `false`
- **FallDamage** (Toggle) — default: `false`
- **MaximumDistance** (Decimal) — default: `200.0`; range: `0.1` – `500.0`

##### Mode: Hypixel

- **Timer** (Decimal) — default: `1.0`; range: `0.1` – `1.0`

##### Mode: HypixelFlat

- **Timer** (Decimal) — default: `1.0`; range: `0.1` – `1.0`
- **Speed** (Decimal) — default: `1.66`; range: `0.8` – `2.0`

#### Visuals

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables visual effects while flying.
- **Stride** (Toggle) — default: `true` — Adds a walking animation while flying.

- **DisableOnSetback** (Toggle) — default: `false` — Disables the module when a server position correction (setback) is detected.

### Screenshots

*Screenshots for Fly will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleFly.kt)*
