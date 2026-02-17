## Velocity

Modifies the amount of velocity you take.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Modify | modes: Modify, Reversal, Strafe, JumpReset, Lag, Hypixel, Dexland, Hylex, BlocksMC, Grim2371, Grim2344-117, AAC4.4.2, Intave)
│   ├── [Mode: Modify]
│   │   ├── Horizontal (Decimal | default: 0.0 | range: -1.0..1.0)
│   │   ├── Vertical (Decimal | default: 0.0 | range: -1.0..1.0)
│   │   ├── MotionHorizontal (Decimal | default: 0.0 | range: 0.0..1.0)
│   │   ├── MotionVertical (Decimal | default: 0.0 | range: 0.0..1.0)
│   │   ├── Chance (Integer | default: 100 | range: 0..100 | %)
│   │   ├── Filter (Choice | default: ALWAYS | options: Always, OnGround, InAir)
│   │   ├── OnlyMove (Toggle | default: false)
│   │   └── TransactionBuffer (Integer | default: 0 | range: 0..3)
│   ├── [Mode: Reversal]
│   │   ├── Delay (Integer | default: 2 | range: 1..5 | ticks)
│   │   ├── XModifier (Decimal | default: 0.5 | range: 0.0..1.0)
│   │   ├── ZModifier (Decimal | default: 0.5 | range: 0.0..1.0)
│   │   └── OnlyMoving (Toggle | default: false)
│   ├── [Mode: Strafe]
│   │   ├── Delay (Integer | default: 2 | range: 0..10 | ticks)
│   │   ├── Strength (Decimal | default: 1.0 | range: 0.1..2.0)
│   │   ├── OnlyFacing (Toggleable Group | default: off)
│   │   │   ├── Enabled (Toggle | default: false)
│   │   │   └── Range (Decimal | default: 3.5 | range: 0.1..6.0)
│   │   └── UntilGround (Toggle | default: false)
│   ├── [Mode: JumpReset]
│   │   ├── Chance (Decimal | default: 100.0 | range: 0.0..100.0 | %)
│   │   ├── JumpByReceivedHits (Toggleable Group | default: off)
│   │   │   ├── Enabled (Toggle | default: false)
│   │   │   └── HitsUntilJump (Integer Range | default: 2..2 | range: 0..10)
│   │   └── JumpByDelay (Toggleable Group | default: on)
│   │       ├── Enabled (Toggle | default: true)
│   │       └── UntilJump (Integer Range | default: 2..2 | range: 0..20 | ticks)
│   ├── [Mode: Lag]
│   │   ├── LagTime (Integer Range | default: 5..5 | range: 1..20 | ticks)
│   │   └── JumpReset (Toggle | default: false)
│   ├── [Mode: Dexland]
│   │   ├── HReduce (Decimal | default: 0.3 | range: 0.0..1.0)
│   │   └── AttacksToWork (Integer | default: 4 | range: 1..10)
│   ├── [Mode: Grim2344-117]
│   │   └── AlternativeBypass (Toggle | default: true)
│   ├── [Mode: AAC4.4.2]
│   │   └── Reduce (Decimal | default: 0.62 | range: 0.0..1.0)
│   └── [Mode: Intave]
│       ├── ReduceOnAttack (Toggleable Group | default: on)
│       │   ├── Enabled (Toggle | default: true)
│       │   ├── Factor (Decimal | default: 0.6 | range: 0.6..1.0)
│       │   ├── HurtTime (Integer Range | default: 5..7 | range: 1..10)
│       │   └── LastAttackTimeToReduce (Integer | default: 2000 | range: 1..10000)
│       └── JumpReset (Toggleable Group | default: on)
│           ├── Enabled (Toggle | default: true)
│           ├── Chance (Decimal | default: 50.0 | range: 0.0..100.0 | %)
│           └── Randomize (Toggleable Group | default: off)
│               ├── Enabled (Toggle | default: false)
│               └── DelayTicks (Integer Range | default: 0..5 | range: 0..10)
├── Delay (Integer Range | default: 0..0 | range: 0..40 | ticks)
└── PauseOnFlag (Integer | default: 0 | range: 0..20 | ticks)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Modify**, **Reversal**, **Strafe**, **JumpReset**, **Lag**, **Hypixel**, **Dexland**, **Hylex**, **BlocksMC**, **Grim2371**, **Grim2344-117**, **AAC4.4.2**, **Intave**. Default: **Modify**.

##### Mode: Modify

- **Horizontal** (Decimal) — default: `0.0`; range: `-1.0` – `1.0` — Multiplier applied to horizontal knockback velocity.
- **Vertical** (Decimal) — default: `0.0`; range: `-1.0` – `1.0` — Multiplier applied to vertical knockback velocity.
- **MotionHorizontal** (Decimal) — default: `0.0`; range: `0.0` – `1.0` — Multiplier applied to existing horizontal motion on knockback.
- **MotionVertical** (Decimal) — default: `0.0`; range: `0.0` – `1.0` — Multiplier applied to existing vertical motion on knockback.
- **Chance** (Integer) — default: `100`; range: `0` – `100`; unit: % — Probability of applying velocity modification per hit.
- **Filter** (Choice) — default: `ALWAYS`; options: `Always`, `OnGround`, `InAir` — Condition filter for when velocity modification applies.
- **OnlyMove** (Toggle) — default: `false` — Only applies modification when the player is moving.
- **TransactionBuffer** (Integer) — default: `0`; range: `0` – `3` — Number of transaction packets to buffer before applying velocity.

##### Mode: Reversal

- **Delay** (Integer) — default: `2`; range: `1` – `5`; unit: ticks — Ticks to wait before reversing the velocity direction.
- **XModifier** (Decimal) — default: `0.5`; range: `0.0` – `1.0` — Multiplier for horizontal X-axis velocity reversal.
- **ZModifier** (Decimal) — default: `0.5`; range: `0.0` – `1.0` — Multiplier for horizontal Z-axis velocity reversal.
- **OnlyMoving** (Toggle) — default: `false` — Only reverses velocity when the player is moving.

##### Mode: Strafe

- **Delay** (Integer) — default: `2`; range: `0` – `10`; unit: ticks — Ticks to wait after knockback before strafing.
- **Strength** (Decimal) — default: `1.0`; range: `0.1` – `2.0` — Strafe movement intensity multiplier.
###### OnlyFacing

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Range** (Decimal) — default: `3.5`; range: `0.1` – `6.0` — Range to check if facing an enemy for strafe activation.

- **UntilGround** (Toggle) — default: `false` — Continues strafing until the player lands on the ground.

##### Mode: JumpReset

- **Chance** (Decimal) — default: `100.0`; range: `0.0` – `100.0`; unit: % — Probability of performing a jump reset on each knockback.
###### JumpByReceivedHits

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **HitsUntilJump** (Integer Range) — default: `2` – `2`; range: `0` – `10` — Number of hits received before triggering a jump.

###### JumpByDelay

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **UntilJump** (Integer Range) — default: `2` – `2`; range: `0` – `20`; unit: ticks — Ticks to wait after knockback before jumping.


##### Mode: Lag

- **LagTime** (Integer Range) — default: `5` – `5`; range: `1` – `20`; unit: ticks — Duration in ticks to delay knockback packets.
- **JumpReset** (Toggle) — default: `false` — Jumps when the lag period ends to reduce remaining velocity.

##### Mode: Dexland

- **HReduce** (Decimal) — default: `0.3`; range: `0.0` – `1.0` — Horizontal velocity reduction factor for Dexland anti-cheat.
- **AttacksToWork** (Integer) — default: `4`; range: `1` – `10` — Number of attacks needed before the reduction activates.

##### Mode: Grim2344-117

- **AlternativeBypass** (Toggle) — default: `true` — Uses an alternative bypass method with duplicate packets.

##### Mode: AAC4.4.2

- **Reduce** (Decimal) — default: `0.62`; range: `0.0` – `1.0` — Velocity reduction factor for AAC 4.4.2 anti-cheat.

##### Mode: Intave

###### ReduceOnAttack

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Factor** (Decimal) — default: `0.6`; range: `0.6` – `1.0` — Velocity reduction multiplier when attacking.
- **HurtTime** (Integer Range) — default: `5` – `7`; range: `1` – `10` — Hurt time window for reduction to apply.
- **LastAttackTimeToReduce** (Integer) — default: `2000`; range: `1` – `10000` — Maximum milliseconds since last attack for reduction to apply.

###### JumpReset

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Chance** (Decimal) — default: `50.0`; range: `0.0` – `100.0`; unit: % — Probability of performing a jump reset for Intave.
###### Randomize

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **DelayTicks** (Integer Range) — default: `0` – `5`; range: `0` – `10` — Random delay in ticks before jumping.



- **Delay** (Integer Range) — default: `0` – `0`; range: `0` – `40`; unit: ticks — Delays velocity packet processing by a random number of ticks.
- **PauseOnFlag** (Integer) — default: `0`; range: `0` – `20`; unit: ticks — Pauses velocity modification for this many ticks when a position correction packet is received.

### Screenshots

*Screenshots for Velocity will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleVelocity.kt)*
