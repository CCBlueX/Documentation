## AutoBuff

Automatically buffs yourself using various items.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Soup (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Health (Integer | default: 40 | range: 1..100 | %HP)
│   ├── ConsiderAbsorption (Toggle | default: true)
│   └── DropAfterUse (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       ├── AssumeEmptyBowl (Toggle | default: true)
│       └── Wait (Integer Range | default: 1..2 | range: 1..20 | ticks)
├── Head (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Health (Integer | default: 40 | range: 1..100 | %HP)
│   ├── ConsiderAbsorption (Toggle | default: true)
│   ├── MaxAbsorption (Decimal | default: 1.0 | range: 0.0..8.0)
│   └── Cooldown (Decimal | default: 0.0 | range: 0.0..120.0 | s)
├── Pot (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Potions (Setting Group)
│   │   ├── Health (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── Health (Integer | default: 40 | range: 1..100 | %HP)
│   │   ├── Regen (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── Health (Integer | default: 40 | range: 1..100 | %HP)
│   │   ├── Strength (Toggleable Group | default: on)
│   │   │   └── Enabled (Toggle | default: true)
│   │   ├── Speed (Toggleable Group | default: on)
│   │   │   └── Enabled (Toggle | default: true)
│   │   ├── FireResistance (Toggleable Group | default: on)
│   │   │   └── Enabled (Toggle | default: true)
│   │   ├── JumpBoost (Toggleable Group | default: on)
│   │   │   └── Enabled (Toggle | default: true)
│   │   └── WaterBreathing (Toggleable Group | default: on)
│   │       └── Enabled (Toggle | default: true)
│   ├── TillGroundDistance (Decimal | default: 2.0 | range: 1.0..5.0)
│   ├── DoNotBenefitOthers (Toggle | default: true)
│   └── AllowLingering (Toggle | default: false)
├── Drink (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Potions (Setting Group)
│       ├── Health (Toggleable Group | default: on)
│       │   ├── Enabled (Toggle | default: true)
│       │   └── Health (Integer | default: 40 | range: 1..100 | %HP)
│       ├── Regen (Toggleable Group | default: on)
│       │   ├── Enabled (Toggle | default: true)
│       │   └── Health (Integer | default: 40 | range: 1..100 | %HP)
│       ├── Strength (Toggleable Group | default: on)
│       │   └── Enabled (Toggle | default: true)
│       ├── Speed (Toggleable Group | default: on)
│       │   └── Enabled (Toggle | default: true)
│       ├── FireResistance (Toggleable Group | default: on)
│       │   └── Enabled (Toggle | default: true)
│       ├── JumpBoost (Toggleable Group | default: on)
│       │   └── Enabled (Toggle | default: true)
│       └── WaterBreathing (Toggleable Group | default: on)
│           └── Enabled (Toggle | default: true)
├── Gapple (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Health (Integer | default: 40 | range: 1..100 | %HP)
│   └── ConsiderAbsorption (Toggle | default: true)
├── AutoSwap (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── DelayIn (Integer Range | default: 1..1 | range: 0..20 | ticks)
│   └── DelayOut (Integer Range | default: 1..1 | range: 0..20 | ticks)
├── Refill (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Constraints (Setting Group)
│       ├── StartDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│       ├── ClickDelay (Integer Range | default: 2..4 | range: 0..20 | ticks)
│       ├── CloseDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│       ├── MissChance (Integer Range | default: 0..0 | range: 0..100 | %)
│       └── Requires (Multi-Select | options: NoMovement, NoRotation, InventoryOpen)
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
│   └── RotationTiming (Choice | default: NORMAL | options: Normal, OnTick, OnUse)
├── CombatPauseTime (Integer | default: 0 | range: 0..40 | ticks)
└── NotDuringCombat (Toggle | default: false)
```

### Settings Details

#### Soup

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Health** (Integer) — default: `40`; range: `1` – `100`; unit: %HP
- **ConsiderAbsorption** (Toggle) — default: `true`
##### DropAfterUse

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **AssumeEmptyBowl** (Toggle) — default: `true`
- **Wait** (Integer Range) — default: `1` – `2`; range: `1` – `20`; unit: ticks


#### Head

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Health** (Integer) — default: `40`; range: `1` – `100`; unit: %HP
- **ConsiderAbsorption** (Toggle) — default: `true`
- **MaxAbsorption** (Decimal) — default: `1.0`; range: `0.0` – `8.0`
- **Cooldown** (Decimal) — default: `0.0`; range: `0.0` – `120.0`; unit: s

#### Pot

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### Potions

A group of related settings.

###### Health

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Health** (Integer) — default: `40`; range: `1` – `100`; unit: %HP

###### Regen

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Health** (Integer) — default: `40`; range: `1` – `100`; unit: %HP

###### Strength

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

###### Speed

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

###### FireResistance

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

###### JumpBoost

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

###### WaterBreathing

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`


- **TillGroundDistance** (Decimal) — default: `2.0`; range: `1.0` – `5.0`
- **DoNotBenefitOthers** (Toggle) — default: `true`
- **AllowLingering** (Toggle) — default: `false`

#### Drink

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### Potions

A group of related settings.

###### Health

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Health** (Integer) — default: `40`; range: `1` – `100`; unit: %HP

###### Regen

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Health** (Integer) — default: `40`; range: `1` – `100`; unit: %HP

###### Strength

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

###### Speed

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

###### FireResistance

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

###### JumpBoost

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`

###### WaterBreathing

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`



#### Gapple

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Health** (Integer) — default: `40`; range: `1` – `100`; unit: %HP
- **ConsiderAbsorption** (Toggle) — default: `true`

#### AutoSwap

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **DelayIn** (Integer Range) — default: `1` – `1`; range: `0` – `20`; unit: ticks
- **DelayOut** (Integer Range) — default: `1` – `1`; range: `0` – `20`; unit: ticks

#### Refill

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### Constraints

A group of related settings.

- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **ClickDelay** (Integer Range) — default: `2` – `4`; range: `0` – `20`; unit: ticks
- **CloseDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **MissChance** (Integer Range) — default: `0` – `0`; range: `0` – `100`; unit: %
- **Requires** (Multi-Select) — options: `NoMovement`, `NoRotation`, `InventoryOpen`


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
- **RotationTiming** (Choice) — default: `NORMAL`; options: `Normal`, `OnTick`, `OnUse`

- **CombatPauseTime** (Integer) — default: `0`; range: `0` – `40`; unit: ticks
- **NotDuringCombat** (Toggle) — default: `false`

### Screenshots

*Screenshots for AutoBuff will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleAutoBuff.kt)*
