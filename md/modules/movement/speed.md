## Speed

Allows you to run faster.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: LegitHop | modes: LegitHop, Custom, YPort, PiercingAttack, VerusB3882, HypixelBHop, HypixelLowHop, Spartan-4.0.4.3, Spartan-4.0.4.3-FastFall, SentinelDamage, Vulcan286, Vulcan288, VulcanGround286, GrimCollide, NCP, Intave14, Intave14Fast, HylexLowHop, HylexGround, BlocksMC, Matrix7)
│   ├── [Mode: Custom]
│   │   ├── HorizontalModification (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   ├── HorizontalAcceleration (Decimal | default: 0.0 | range: -0.1..0.2)
│   │   │   ├── HorizontalJumpOff (Decimal | default: 0.0 | range: -0.5..1.0)
│   │   │   └── TicksToBoostOff (Integer | default: 0 | range: 0..20 | ticks)
│   │   ├── VerticalModification (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   ├── JumpHeight (Decimal | default: 0.42 | range: 0.0..3.0)
│   │   │   ├── Pulldown (Decimal | default: 0.0 | range: 0.0..1.0)
│   │   │   └── PullDownDuringFall (Decimal | default: 0.0 | range: 0.0..1.0)
│   │   ├── TimerSpeed (Decimal | default: 1.0 | range: 0.1..10.0)
│   │   └── Strafe (Toggleable Group | default: on)
│   │       ├── Enabled (Toggle | default: true)
│   │       ├── Strength (Decimal | default: 1.0 | range: 0.1..1.0)
│   │       ├── CustomSpeed (Toggle | default: false)
│   │       ├── Speed (Decimal | default: 1.0 | range: 0.1..10.0)
│   │       ├── VelocityTimeout (Integer | default: 0 | range: 0..20 | ticks)
│   │       └── StrafeKnock (Toggle | default: false)
│   ├── [Mode: YPort]
│   │   └── Speed (Decimal | default: 0.4 | range: 0.1..1.0)
│   ├── [Mode: PiercingAttack]
│   │   ├── SwingMode (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│   │   ├── HoldTime (Integer Range | default: 1..1 | range: 1..20 | ticks)
│   │   ├── OnGround (Toggle | default: true)
│   │   ├── IgnoreHunger (Toggle | default: false)
│   │   ├── WaitForCooldown (Toggle | default: true)
│   │   └── MinimumDurability (Integer | default: 1 | range: 0..20)
│   ├── [Mode: HypixelBHop]
│   │   ├── HorizontalAcceleration (Toggle | default: true)
│   │   └── VerticalAcceleration (Toggle | default: true)
│   ├── [Mode: HypixelLowHop]
│   │   └── Glide (Toggle | default: false)
│   ├── [Mode: SentinelDamage]
│   │   ├── Speed (Decimal | default: 0.5 | range: 0.1..5.0)
│   │   └── ReboostTicks (Integer | default: 30 | range: 10..50)
│   ├── [Mode: GrimCollide]
│   │   ├── BoostSpeed (Decimal | default: 0.08 | range: 0.01..0.08 | b/t)
│   │   └── ShrinkBox (Decimal | default: 0.5 | range: 0.1..2.0)
│   ├── [Mode: NCP]
│   │   ├── PullDown (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   ├── MotionMultiplier (Decimal | default: 1.0 | range: 0.01..10.0)
│   │   │   ├── OnTick (Integer | default: 5 | range: 1..9)
│   │   │   └── OnHurt (Toggle | default: true)
│   │   ├── Boost (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── InitialBoostMultiplier (Decimal | default: 1.0 | range: 0.01..10.0)
│   │   ├── Timer (Toggle | default: true)
│   │   ├── DamageBoost (Toggle | default: true)
│   │   ├── LowHop (Toggle | default: true)
│   │   └── AirStrafe (Toggle | default: true)
│   ├── [Mode: Intave14]
│   │   ├── Strafe (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── Strength (Decimal | default: 0.27 | range: 0.01..0.27)
│   │   └── AirBoost (Toggleable Group | default: on)
│   │       └── Enabled (Toggle | default: true)
│   ├── [Mode: Intave14Fast]
│   │   └── Timer (Toggle | default: true)
│   ├── [Mode: BlocksMC]
│   │   └── RoundStrafeYaw (Toggle | default: false)
├── Not (Multi-Select | default: [DuringScaffold] | options: WhileUsingItem, DuringScaffold, WhileSneaking)
├── AvoidEdgeBump (Toggle | default: true)
├── OnlyInCombat (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   └── Mode (Mode Selector | default: LegitHop | modes: LegitHop, Custom, YPort, PiercingAttack, VerusB3882, HypixelBHop, HypixelLowHop, Spartan-4.0.4.3, Spartan-4.0.4.3-FastFall, SentinelDamage, Vulcan286, Vulcan288, VulcanGround286, GrimCollide, NCP, Intave14, Intave14Fast, HylexLowHop, HylexGround, BlocksMC, Matrix7)
│       ├── [Mode: Custom]
│       │   ├── HorizontalModification (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   ├── HorizontalAcceleration (Decimal | default: 0.0 | range: -0.1..0.2)
│       │   │   ├── HorizontalJumpOff (Decimal | default: 0.0 | range: -0.5..1.0)
│       │   │   └── TicksToBoostOff (Integer | default: 0 | range: 0..20 | ticks)
│       │   ├── VerticalModification (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   ├── JumpHeight (Decimal | default: 0.42 | range: 0.0..3.0)
│       │   │   ├── Pulldown (Decimal | default: 0.0 | range: 0.0..1.0)
│       │   │   └── PullDownDuringFall (Decimal | default: 0.0 | range: 0.0..1.0)
│       │   ├── TimerSpeed (Decimal | default: 1.0 | range: 0.1..10.0)
│       │   └── Strafe (Toggleable Group | default: on)
│       │       ├── Enabled (Toggle | default: true)
│       │       ├── Strength (Decimal | default: 1.0 | range: 0.1..1.0)
│       │       ├── CustomSpeed (Toggle | default: false)
│       │       ├── Speed (Decimal | default: 1.0 | range: 0.1..10.0)
│       │       ├── VelocityTimeout (Integer | default: 0 | range: 0..20 | ticks)
│       │       └── StrafeKnock (Toggle | default: false)
│       ├── [Mode: YPort]
│       │   └── Speed (Decimal | default: 0.4 | range: 0.1..1.0)
│       ├── [Mode: PiercingAttack]
│       │   ├── SwingMode (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│       │   ├── HoldTime (Integer Range | default: 1..1 | range: 1..20 | ticks)
│       │   ├── OnGround (Toggle | default: true)
│       │   ├── IgnoreHunger (Toggle | default: false)
│       │   ├── WaitForCooldown (Toggle | default: true)
│       │   └── MinimumDurability (Integer | default: 1 | range: 0..20)
│       ├── [Mode: HypixelBHop]
│       │   ├── HorizontalAcceleration (Toggle | default: true)
│       │   └── VerticalAcceleration (Toggle | default: true)
│       ├── [Mode: HypixelLowHop]
│       │   └── Glide (Toggle | default: false)
│       ├── [Mode: SentinelDamage]
│       │   ├── Speed (Decimal | default: 0.5 | range: 0.1..5.0)
│       │   └── ReboostTicks (Integer | default: 30 | range: 10..50)
│       ├── [Mode: GrimCollide]
│       │   ├── BoostSpeed (Decimal | default: 0.08 | range: 0.01..0.08 | b/t)
│       │   └── ShrinkBox (Decimal | default: 0.5 | range: 0.1..2.0)
│       ├── [Mode: NCP]
│       │   ├── PullDown (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   ├── MotionMultiplier (Decimal | default: 1.0 | range: 0.01..10.0)
│       │   │   ├── OnTick (Integer | default: 5 | range: 1..9)
│       │   │   └── OnHurt (Toggle | default: true)
│       │   ├── Boost (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   └── InitialBoostMultiplier (Decimal | default: 1.0 | range: 0.01..10.0)
│       │   ├── Timer (Toggle | default: true)
│       │   ├── DamageBoost (Toggle | default: true)
│       │   ├── LowHop (Toggle | default: true)
│       │   └── AirStrafe (Toggle | default: true)
│       ├── [Mode: Intave14]
│       │   ├── Strafe (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   └── Strength (Decimal | default: 0.27 | range: 0.01..0.27)
│       │   └── AirBoost (Toggleable Group | default: on)
│       │       └── Enabled (Toggle | default: true)
│       ├── [Mode: Intave14Fast]
│       │   └── Timer (Toggle | default: true)
│       ├── [Mode: BlocksMC]
│       │   └── RoundStrafeYaw (Toggle | default: false)
├── OnlyOnPotionEffect (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── PotionEffect (Mode Selector | default: Speed | modes: Speed, Slowness, Both)
│   │   ├── [Mode: Speed]
│   │   │   └── LevelRange (Integer Range | default: 1..2 | range: 0..4)
│   │   ├── [Mode: Slowness]
│   │   │   └── LevelRange (Integer Range | default: 1..2 | range: 0..4)
│   │   └── [Mode: Both]
│   │       └── PotionEffectsBoostRange (Decimal Range | default: 1.15..1.35 | range: 0.25..2.0)
│   └── Mode (Mode Selector | default: LegitHop | modes: LegitHop, Custom, YPort, PiercingAttack, VerusB3882, HypixelBHop, HypixelLowHop, Spartan-4.0.4.3, Spartan-4.0.4.3-FastFall, SentinelDamage, Vulcan286, Vulcan288, VulcanGround286, GrimCollide, NCP, Intave14, Intave14Fast, HylexLowHop, HylexGround, BlocksMC, Matrix7)
│       ├── [Mode: Custom]
│       │   ├── HorizontalModification (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   ├── HorizontalAcceleration (Decimal | default: 0.0 | range: -0.1..0.2)
│       │   │   ├── HorizontalJumpOff (Decimal | default: 0.0 | range: -0.5..1.0)
│       │   │   └── TicksToBoostOff (Integer | default: 0 | range: 0..20 | ticks)
│       │   ├── VerticalModification (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   ├── JumpHeight (Decimal | default: 0.42 | range: 0.0..3.0)
│       │   │   ├── Pulldown (Decimal | default: 0.0 | range: 0.0..1.0)
│       │   │   └── PullDownDuringFall (Decimal | default: 0.0 | range: 0.0..1.0)
│       │   ├── TimerSpeed (Decimal | default: 1.0 | range: 0.1..10.0)
│       │   └── Strafe (Toggleable Group | default: on)
│       │       ├── Enabled (Toggle | default: true)
│       │       ├── Strength (Decimal | default: 1.0 | range: 0.1..1.0)
│       │       ├── CustomSpeed (Toggle | default: false)
│       │       ├── Speed (Decimal | default: 1.0 | range: 0.1..10.0)
│       │       ├── VelocityTimeout (Integer | default: 0 | range: 0..20 | ticks)
│       │       └── StrafeKnock (Toggle | default: false)
│       ├── [Mode: YPort]
│       │   └── Speed (Decimal | default: 0.4 | range: 0.1..1.0)
│       ├── [Mode: PiercingAttack]
│       │   ├── SwingMode (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│       │   ├── HoldTime (Integer Range | default: 1..1 | range: 1..20 | ticks)
│       │   ├── OnGround (Toggle | default: true)
│       │   ├── IgnoreHunger (Toggle | default: false)
│       │   ├── WaitForCooldown (Toggle | default: true)
│       │   └── MinimumDurability (Integer | default: 1 | range: 0..20)
│       ├── [Mode: HypixelBHop]
│       │   ├── HorizontalAcceleration (Toggle | default: true)
│       │   └── VerticalAcceleration (Toggle | default: true)
│       ├── [Mode: HypixelLowHop]
│       │   └── Glide (Toggle | default: false)
│       ├── [Mode: SentinelDamage]
│       │   ├── Speed (Decimal | default: 0.5 | range: 0.1..5.0)
│       │   └── ReboostTicks (Integer | default: 30 | range: 10..50)
│       ├── [Mode: GrimCollide]
│       │   ├── BoostSpeed (Decimal | default: 0.08 | range: 0.01..0.08 | b/t)
│       │   └── ShrinkBox (Decimal | default: 0.5 | range: 0.1..2.0)
│       ├── [Mode: NCP]
│       │   ├── PullDown (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   ├── MotionMultiplier (Decimal | default: 1.0 | range: 0.01..10.0)
│       │   │   ├── OnTick (Integer | default: 5 | range: 1..9)
│       │   │   └── OnHurt (Toggle | default: true)
│       │   ├── Boost (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   └── InitialBoostMultiplier (Decimal | default: 1.0 | range: 0.01..10.0)
│       │   ├── Timer (Toggle | default: true)
│       │   ├── DamageBoost (Toggle | default: true)
│       │   ├── LowHop (Toggle | default: true)
│       │   └── AirStrafe (Toggle | default: true)
│       ├── [Mode: Intave14]
│       │   ├── Strafe (Toggleable Group | default: on)
│       │   │   ├── Enabled (Toggle | default: true)
│       │   │   └── Strength (Decimal | default: 0.27 | range: 0.01..0.27)
│       │   └── AirBoost (Toggleable Group | default: on)
│       │       └── Enabled (Toggle | default: true)
│       ├── [Mode: Intave14Fast]
│       │   └── Timer (Toggle | default: true)
│       ├── [Mode: BlocksMC]
│       │   └── RoundStrafeYaw (Toggle | default: false)
└── YawOffset (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    └── YawOffsetMode (Choice | default: AIR | options: Ground, Air, Constant)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **LegitHop**, **Custom**, **YPort**, **PiercingAttack**, **VerusB3882**, **HypixelBHop**, **HypixelLowHop**, **Spartan-4.0.4.3**, **Spartan-4.0.4.3-FastFall**, **SentinelDamage**, **Vulcan286**, **Vulcan288**, **VulcanGround286**, **GrimCollide**, **NCP**, **Intave14**, **Intave14Fast**, **HylexLowHop**, **HylexGround**, **BlocksMC**, **Matrix7**. Default: **LegitHop**.

##### Mode: Custom

###### HorizontalModification

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **HorizontalAcceleration** (Decimal) — default: `0.0`; range: `-0.1` – `0.2`
- **HorizontalJumpOff** (Decimal) — default: `0.0`; range: `-0.5` – `1.0`
- **TicksToBoostOff** (Integer) — default: `0`; range: `0` – `20`; unit: ticks

###### VerticalModification

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **JumpHeight** (Decimal) — default: `0.42`; range: `0.0` – `3.0`
- **Pulldown** (Decimal) — default: `0.0`; range: `0.0` – `1.0`
- **PullDownDuringFall** (Decimal) — default: `0.0`; range: `0.0` – `1.0`

- **TimerSpeed** (Decimal) — default: `1.0`; range: `0.1` – `10.0`
###### Strafe

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Strength** (Decimal) — default: `1.0`; range: `0.1` – `1.0`
- **CustomSpeed** (Toggle) — default: `false`
- **Speed** (Decimal) — default: `1.0`; range: `0.1` – `10.0`
- **VelocityTimeout** (Integer) — default: `0`; range: `0` – `20`; unit: ticks
- **StrafeKnock** (Toggle) — default: `false`


##### Mode: YPort

- **Speed** (Decimal) — default: `0.4`; range: `0.1` – `1.0`

##### Mode: PiercingAttack

- **SwingMode** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **HoldTime** (Integer Range) — default: `1` – `1`; range: `1` – `20`; unit: ticks
- **OnGround** (Toggle) — default: `true`
- **IgnoreHunger** (Toggle) — default: `false`
- **WaitForCooldown** (Toggle) — default: `true`
- **MinimumDurability** (Integer) — default: `1`; range: `0` – `20`

##### Mode: HypixelBHop

- **HorizontalAcceleration** (Toggle) — default: `true`
- **VerticalAcceleration** (Toggle) — default: `true`

##### Mode: HypixelLowHop

- **Glide** (Toggle) — default: `false`

##### Mode: SentinelDamage

- **Speed** (Decimal) — default: `0.5`; range: `0.1` – `5.0`
- **ReboostTicks** (Integer) — default: `30`; range: `10` – `50`

##### Mode: GrimCollide

- **BoostSpeed** (Decimal) — default: `0.08`; range: `0.01` – `0.08`; unit: b/t
- **ShrinkBox** (Decimal) — default: `0.5`; range: `0.1` – `2.0`

##### Mode: NCP

###### PullDown

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **MotionMultiplier** (Decimal) — default: `1.0`; range: `0.01` – `10.0`
- **OnTick** (Integer) — default: `5`; range: `1` – `9`
- **OnHurt** (Toggle) — default: `true`

###### Boost

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **InitialBoostMultiplier** (Decimal) — default: `1.0`; range: `0.01` – `10.0`

- **Timer** (Toggle) — default: `true`
- **DamageBoost** (Toggle) — default: `true`
- **LowHop** (Toggle) — default: `true`
- **AirStrafe** (Toggle) — default: `true`

##### Mode: Intave14

###### Strafe

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Strength** (Decimal) — default: `0.27`; range: `0.01` – `0.27`

###### AirBoost

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`


##### Mode: Intave14Fast

- **Timer** (Toggle) — default: `true`

##### Mode: BlocksMC

- **RoundStrafeYaw** (Toggle) — default: `false`

- **Not** (Multi-Select) — default: `DuringScaffold`; options: `WhileUsingItem`, `DuringScaffold`, `WhileSneaking`
- **AvoidEdgeBump** (Toggle) — default: `true`
#### OnlyInCombat

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
##### Mode

Select a mode for this feature. Available modes: **LegitHop**, **Custom**, **YPort**, **PiercingAttack**, **VerusB3882**, **HypixelBHop**, **HypixelLowHop**, **Spartan-4.0.4.3**, **Spartan-4.0.4.3-FastFall**, **SentinelDamage**, **Vulcan286**, **Vulcan288**, **VulcanGround286**, **GrimCollide**, **NCP**, **Intave14**, **Intave14Fast**, **HylexLowHop**, **HylexGround**, **BlocksMC**, **Matrix7**. Default: **LegitHop**.

###### Mode: Custom

###### HorizontalModification

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **HorizontalAcceleration** (Decimal) — default: `0.0`; range: `-0.1` – `0.2`
- **HorizontalJumpOff** (Decimal) — default: `0.0`; range: `-0.5` – `1.0`
- **TicksToBoostOff** (Integer) — default: `0`; range: `0` – `20`; unit: ticks

###### VerticalModification

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **JumpHeight** (Decimal) — default: `0.42`; range: `0.0` – `3.0`
- **Pulldown** (Decimal) — default: `0.0`; range: `0.0` – `1.0`
- **PullDownDuringFall** (Decimal) — default: `0.0`; range: `0.0` – `1.0`

- **TimerSpeed** (Decimal) — default: `1.0`; range: `0.1` – `10.0`
###### Strafe

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Strength** (Decimal) — default: `1.0`; range: `0.1` – `1.0`
- **CustomSpeed** (Toggle) — default: `false`
- **Speed** (Decimal) — default: `1.0`; range: `0.1` – `10.0`
- **VelocityTimeout** (Integer) — default: `0`; range: `0` – `20`; unit: ticks
- **StrafeKnock** (Toggle) — default: `false`


###### Mode: YPort

- **Speed** (Decimal) — default: `0.4`; range: `0.1` – `1.0`

###### Mode: PiercingAttack

- **SwingMode** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **HoldTime** (Integer Range) — default: `1` – `1`; range: `1` – `20`; unit: ticks
- **OnGround** (Toggle) — default: `true`
- **IgnoreHunger** (Toggle) — default: `false`
- **WaitForCooldown** (Toggle) — default: `true`
- **MinimumDurability** (Integer) — default: `1`; range: `0` – `20`

###### Mode: HypixelBHop

- **HorizontalAcceleration** (Toggle) — default: `true`
- **VerticalAcceleration** (Toggle) — default: `true`

###### Mode: HypixelLowHop

- **Glide** (Toggle) — default: `false`

###### Mode: SentinelDamage

- **Speed** (Decimal) — default: `0.5`; range: `0.1` – `5.0`
- **ReboostTicks** (Integer) — default: `30`; range: `10` – `50`

###### Mode: GrimCollide

- **BoostSpeed** (Decimal) — default: `0.08`; range: `0.01` – `0.08`; unit: b/t
- **ShrinkBox** (Decimal) — default: `0.5`; range: `0.1` – `2.0`

###### Mode: NCP

###### PullDown

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **MotionMultiplier** (Decimal) — default: `1.0`; range: `0.01` – `10.0`
- **OnTick** (Integer) — default: `5`; range: `1` – `9`
- **OnHurt** (Toggle) — default: `true`

###### Boost

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **InitialBoostMultiplier** (Decimal) — default: `1.0`; range: `0.01` – `10.0`

- **Timer** (Toggle) — default: `true`
- **DamageBoost** (Toggle) — default: `true`
- **LowHop** (Toggle) — default: `true`
- **AirStrafe** (Toggle) — default: `true`

###### Mode: Intave14

###### Strafe

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Strength** (Decimal) — default: `0.27`; range: `0.01` – `0.27`

###### AirBoost

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`


###### Mode: Intave14Fast

- **Timer** (Toggle) — default: `true`

###### Mode: BlocksMC

- **RoundStrafeYaw** (Toggle) — default: `false`


#### OnlyOnPotionEffect

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
##### PotionEffect

Select a mode for this feature. Available modes: **Speed**, **Slowness**, **Both**. Default: **Speed**.

###### Mode: Speed

- **LevelRange** (Integer Range) — default: `1` – `2`; range: `0` – `4`

###### Mode: Slowness

- **LevelRange** (Integer Range) — default: `1` – `2`; range: `0` – `4`

###### Mode: Both

- **PotionEffectsBoostRange** (Decimal Range) — default: `1.15` – `1.35`; range: `0.25` – `2.0`

##### Mode

Select a mode for this feature. Available modes: **LegitHop**, **Custom**, **YPort**, **PiercingAttack**, **VerusB3882**, **HypixelBHop**, **HypixelLowHop**, **Spartan-4.0.4.3**, **Spartan-4.0.4.3-FastFall**, **SentinelDamage**, **Vulcan286**, **Vulcan288**, **VulcanGround286**, **GrimCollide**, **NCP**, **Intave14**, **Intave14Fast**, **HylexLowHop**, **HylexGround**, **BlocksMC**, **Matrix7**. Default: **LegitHop**.

###### Mode: Custom

###### HorizontalModification

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **HorizontalAcceleration** (Decimal) — default: `0.0`; range: `-0.1` – `0.2`
- **HorizontalJumpOff** (Decimal) — default: `0.0`; range: `-0.5` – `1.0`
- **TicksToBoostOff** (Integer) — default: `0`; range: `0` – `20`; unit: ticks

###### VerticalModification

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **JumpHeight** (Decimal) — default: `0.42`; range: `0.0` – `3.0`
- **Pulldown** (Decimal) — default: `0.0`; range: `0.0` – `1.0`
- **PullDownDuringFall** (Decimal) — default: `0.0`; range: `0.0` – `1.0`

- **TimerSpeed** (Decimal) — default: `1.0`; range: `0.1` – `10.0`
###### Strafe

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Strength** (Decimal) — default: `1.0`; range: `0.1` – `1.0`
- **CustomSpeed** (Toggle) — default: `false`
- **Speed** (Decimal) — default: `1.0`; range: `0.1` – `10.0`
- **VelocityTimeout** (Integer) — default: `0`; range: `0` – `20`; unit: ticks
- **StrafeKnock** (Toggle) — default: `false`


###### Mode: YPort

- **Speed** (Decimal) — default: `0.4`; range: `0.1` – `1.0`

###### Mode: PiercingAttack

- **SwingMode** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **HoldTime** (Integer Range) — default: `1` – `1`; range: `1` – `20`; unit: ticks
- **OnGround** (Toggle) — default: `true`
- **IgnoreHunger** (Toggle) — default: `false`
- **WaitForCooldown** (Toggle) — default: `true`
- **MinimumDurability** (Integer) — default: `1`; range: `0` – `20`

###### Mode: HypixelBHop

- **HorizontalAcceleration** (Toggle) — default: `true`
- **VerticalAcceleration** (Toggle) — default: `true`

###### Mode: HypixelLowHop

- **Glide** (Toggle) — default: `false`

###### Mode: SentinelDamage

- **Speed** (Decimal) — default: `0.5`; range: `0.1` – `5.0`
- **ReboostTicks** (Integer) — default: `30`; range: `10` – `50`

###### Mode: GrimCollide

- **BoostSpeed** (Decimal) — default: `0.08`; range: `0.01` – `0.08`; unit: b/t
- **ShrinkBox** (Decimal) — default: `0.5`; range: `0.1` – `2.0`

###### Mode: NCP

###### PullDown

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **MotionMultiplier** (Decimal) — default: `1.0`; range: `0.01` – `10.0`
- **OnTick** (Integer) — default: `5`; range: `1` – `9`
- **OnHurt** (Toggle) — default: `true`

###### Boost

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **InitialBoostMultiplier** (Decimal) — default: `1.0`; range: `0.01` – `10.0`

- **Timer** (Toggle) — default: `true`
- **DamageBoost** (Toggle) — default: `true`
- **LowHop** (Toggle) — default: `true`
- **AirStrafe** (Toggle) — default: `true`

###### Mode: Intave14

###### Strafe

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Strength** (Decimal) — default: `0.27`; range: `0.01` – `0.27`

###### AirBoost

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`


###### Mode: Intave14Fast

- **Timer** (Toggle) — default: `true`

###### Mode: BlocksMC

- **RoundStrafeYaw** (Toggle) — default: `false`


#### YawOffset

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **YawOffsetMode** (Choice) — default: `AIR`; options: `Ground`, `Air`, `Constant`


### Screenshots

*Screenshots for Speed will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleSpeed.kt)*
