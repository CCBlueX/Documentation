## AutoFarm

Automatically farms crops.

**Category:** World  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Range (Decimal | default: 5.0 | range: 1.0..6.0)
├── WallRange (Decimal | default: 0.0 | range: 0.0..6.0)
├── InteractDelay (Integer Range | default: 2..3 | range: 1..15 | ticks)
├── DisableOnFullInventory (Toggle | default: false)
├── UseFortune (Toggle | default: true)
├── AutoWalk (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── Auto (Multi-Select | default: [Jump, Swim, Sprint] | options: Jump, Swim, Sprint)
│   ├── MinimumDistance (Decimal | default: 2.0 | range: 1.0..4.0)
│   ├── ToPlant (Toggle | default: true)
│   └── ToItems (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       ├── Range (Decimal | default: 20.0 | range: 8.0..64.0)
│       ├── Items (Registry List)
│       └── Filter (Choice | default: BLACKLIST | options: Whitelist, Blacklist)
├── AutoPlant (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── SwapBackDelay (Integer Range | default: 1..2 | range: 1..20 | ticks)
├── AutoUseBoneMeal (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── UseDelay (Integer Range | default: 20..200 | range: 0..20000 | ms)
│   └── SwapBackDelay (Integer Range | default: 1..2 | range: 1..20 | ticks)
├── Visualize (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Path (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   └── PathColor (Color)
│   └── Blocks (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       ├── Outline (Toggle | default: true)
│       ├── ReadyColor (Color)
│       ├── PlaceColor (Color)
│       ├── Range (Integer | default: 50 | range: 10..128)
│       ├── Rainbow (Toggle | default: false)
│       └── PlaceTargets (Multi-Select | default: [Farmland, SoulSand, JungleLogs] | options: Farmland, SoulSand, JungleLogs)
└── Rotations (Setting Group)
    ├── AngleSmooth (Mode Selector | default: Linear | modes: Linear, Sigmoid, Acceleration)
    │   ├── [Mode: Linear]
    │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
    │   │   └── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
    │   ├── [Mode: Sigmoid]
    │   │   ├── HorizontalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
    │   │   ├── VerticalTurnSpeed (Decimal Range | default: 180.0..180.0 | range: 0.0..180.0)
    │   │   ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
    │   │   └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
    │   └── [Mode: Acceleration]
    │       ├── YawAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
    │       ├── PitchAcceleration (Decimal Range | default: 20.0..25.0 | range: 1.0..180.0)
    │       ├── DynamicAccel (Toggleable Group | default: off)
    │       │   ├── Enabled (Toggle | default: false)
    │       │   ├── CoefDistance (Decimal | default: -1.393 | range: -2.0..2.0)
    │       │   ├── YawCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
    │       │   └── PitchCrosshairAccel (Decimal Range | default: 17.0..20.0 | range: 1.0..180.0)
    │       ├── AccelerationError (Toggleable Group | default: on)
    │       │   ├── Enabled (Toggle | default: true)
    │       │   ├── YawAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
    │       │   └── PitchAccelError (Decimal | default: 0.1 | range: 0.01..1.0)
    │       ├── ConstantError (Toggleable Group | default: on)
    │       │   ├── Enabled (Toggle | default: true)
    │       │   ├── YawConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
    │       │   └── PitchConstantError (Decimal | default: 0.1 | range: 0.01..1.0)
    │       └── SigmoidDeceleration (Toggleable Group | default: off)
    │           ├── Enabled (Toggle | default: false)
    │           ├── Steepness (Decimal | default: 10.0 | range: 0.0..20.0)
    │           └── Midpoint (Decimal | default: 0.3 | range: 0.0..1.0)
    ├── MovementCorrection (Choice | default: SILENT | options: Off, Strict, Silent, ChangeLook)
    ├── ResetThreshold (Decimal | default: 2.0 | range: 1.0..180.0)
    └── TicksUntilReset (Integer | default: 5 | range: 1..30 | ticks)
```

### Settings Details

- **Range** (Decimal) — default: `5.0`; range: `1.0` – `6.0`
- **WallRange** (Decimal) — default: `0.0`; range: `0.0` – `6.0`
- **InteractDelay** (Integer Range) — default: `2` – `3`; range: `1` – `15`; unit: ticks
- **DisableOnFullInventory** (Toggle) — default: `false`
- **UseFortune** (Toggle) — default: `true`
#### AutoWalk

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Auto** (Multi-Select) — default: `Jump`, `Swim`, `Sprint`; options: `Jump`, `Swim`, `Sprint`
- **MinimumDistance** (Decimal) — default: `2.0`; range: `1.0` – `4.0`
- **ToPlant** (Toggle) — default: `true`
##### ToItems

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Range** (Decimal) — default: `20.0`; range: `8.0` – `64.0`
- **Items** (Registry List)
- **Filter** (Choice) — default: `BLACKLIST`; options: `Whitelist`, `Blacklist`


#### AutoPlant

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **SwapBackDelay** (Integer Range) — default: `1` – `2`; range: `1` – `20`; unit: ticks

#### AutoUseBoneMeal

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **UseDelay** (Integer Range) — default: `20` – `200`; range: `0` – `20000`; unit: ms
- **SwapBackDelay** (Integer Range) — default: `1` – `2`; range: `1` – `20`; unit: ticks

#### Visualize

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### Path

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **PathColor** (Color)

##### Blocks

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Outline** (Toggle) — default: `true`
- **ReadyColor** (Color)
- **PlaceColor** (Color)
- **Range** (Integer) — default: `50`; range: `10` – `128`
- **Rainbow** (Toggle) — default: `false`
- **PlaceTargets** (Multi-Select) — default: `Farmland`, `SoulSand`, `JungleLogs`; options: `Farmland`, `SoulSand`, `JungleLogs`


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


### Screenshots

*Screenshots for AutoFarm will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2FModuleAutoFarm.kt)*
