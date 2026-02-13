## ElytraFly

Makes controlling an elytra easier.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Instant (Multi-Select | default: [Stop] | options: Start, Stop)
├── NotInFluid (Toggle | default: false)
├── DurabilityExploit (Toggle | default: false)
├── Speed (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Vertical (Decimal | default: 0.5 | range: 0.0..5.0)
│   └── Horizontal (Decimal | default: 1.0 | range: 0.0..8.0)
└── Mode (Mode Selector | default: Static | modes: Static, Vanilla, Boost, Firework, Pitch40Infinite)
    ├── [Mode: Static]
    │   ├── DurabilityExploitNotWhileNoMove (Toggle | default: false)
    │   └── Glide (Toggleable Group | default: off)
    │       ├── Enabled (Toggle | default: false)
    │       ├── Vertical (Decimal | default: 0.01 | range: 0.0..1.0)
    │       └── Horizontal (Decimal | default: 0.0 | range: 0.0..1.0)
    ├── [Mode: Boost]
    │   ├── Speed (Decimal | default: 0.9 | range: 0.5..2.0)
    │   ├── Acceleration (Decimal | default: 0.01 | range: 0.005..0.05)
    │   ├── AutoBoost (Toggle | default: true)
    │   ├── VerticalControl (Decimal | default: 0.8 | range: 0.2..1.0)
    │   ├── SmartGroundBehavior (Toggle | default: true)
    │   ├── GroundDistance (Decimal | default: 3.0 | range: 1.5..7.0)
    │   ├── DiveMechanics (Toggle | default: true)
    │   ├── DiveAcceleration (Decimal | default: 0.05 | range: 0.01..0.1)
    │   └── DiveEfficiency (Decimal | default: 0.8 | range: 0.4..1.5)
    ├── [Mode: Firework]
    │   ├── ConsiderInventory (Toggleable Group | default: off)
    │   │   ├── Enabled (Toggle | default: false)
    │   │   └── Constraints (Setting Group)
    │   │       ├── StartDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
    │   │       ├── ClickDelay (Integer Range | default: 2..4 | range: 0..20 | ticks)
    │   │       ├── CloseDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
    │   │       ├── MissChance (Integer Range | default: 0..0 | range: 0..100 | %)
    │   │       └── Requires (Multi-Select | options: NoMovement, NoRotation, InventoryOpen)
    │   └── Cooldown (Integer Range | default: 20..20 | range: 0..300 | ticks)
    └── [Mode: Pitch40Infinite]
        ├── MinSpeed (Decimal | default: 25.0 | range: 10.0..70.0)
        ├── MaxSpeed (Decimal | default: 150.0 | range: 50.0..170.0)
        ├── MaxHeight (Integer | default: 200 | range: 50..360)
        └── PitchIncrement (Decimal | default: 3.0 | range: 1.0..10.0)
```

### Settings Details

- **Instant** (Multi-Select) — default: `Stop`; options: `Start`, `Stop` — Start instantly begins elytra flight when jumping, Stop lands when sneaking on the ground.
- **NotInFluid** (Toggle) — default: `false` — Stops elytra flight when entering a liquid.
- **DurabilityExploit** (Toggle) — default: `false` — Rapidly toggles elytra flight to avoid consuming durability.
#### Speed

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables the speed override group.
- **Vertical** (Decimal) — default: `0.5`; range: `0.0` – `5.0` — Vertical flight speed while holding jump or sneak.
- **Horizontal** (Decimal) — default: `1.0`; range: `0.0` – `8.0` — Horizontal flight speed while moving.

#### Mode

Select a mode for this feature. Available modes: **Static**, **Vanilla**, **Boost**, **Firework**, **Pitch40Infinite**. Default: **Static**.

##### Mode: Static

- **DurabilityExploitNotWhileNoMove** (Toggle) — default: `false` — Only runs the durability exploit while the player is not moving.
###### Glide

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Enables the glide effect when not moving.
- **Vertical** (Decimal) — default: `0.01`; range: `0.0` – `1.0` — Downward glide speed when not moving.
- **Horizontal** (Decimal) — default: `0.0`; range: `0.0` – `1.0` — Horizontal glide speed when not moving.


##### Mode: Boost

- **Speed** (Decimal) — default: `0.9`; range: `0.5` – `2.0` — Maximum boost speed.
- **Acceleration** (Decimal) — default: `0.01`; range: `0.005` – `0.05` — Rate at which speed increases toward the maximum.
- **AutoBoost** (Toggle) — default: `true` — Automatically boosts when looking up and not near the ground.
- **VerticalControl** (Decimal) — default: `0.8`; range: `0.2` – `1.0` — Multiplier for vertical speed when using jump/sneak keys.
- **SmartGroundBehavior** (Toggle) — default: `true` — Adjusts flight behavior when near the ground.
- **GroundDistance** (Decimal) — default: `3.0`; range: `1.5` – `7.0` — Distance in blocks to detect ground proximity.
- **DiveMechanics** (Toggle) — default: `true` — Enables gaining speed by diving downward and converting it on pull-up.
- **DiveAcceleration** (Decimal) — default: `0.05`; range: `0.01` – `0.1` — How quickly dive speed builds up while looking down.
- **DiveEfficiency** (Decimal) — default: `0.8`; range: `0.4` – `1.5` — How efficiently stored dive speed converts into lift on pull-up.

##### Mode: Firework

###### ConsiderInventory

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Enables inventory management for finding fireworks outside the hotbar.
###### Constraints

A group of related settings.

- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **ClickDelay** (Integer Range) — default: `2` – `4`; range: `0` – `20`; unit: ticks
- **CloseDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **MissChance** (Integer Range) — default: `0` – `0`; range: `0` – `100`; unit: %
- **Requires** (Multi-Select) — options: `NoMovement`, `NoRotation`, `InventoryOpen`


- **Cooldown** (Integer Range) — default: `20` – `20`; range: `0` – `300`; unit: ticks — Delay in ticks between firework uses.

##### Mode: Pitch40Infinite

- **MinSpeed** (Decimal) — default: `25.0`; range: `10.0` – `70.0` — Speed in km/h below which the pitch cycles upward to gain altitude.
- **MaxSpeed** (Decimal) — default: `150.0`; range: `50.0` – `170.0` — Speed in km/h above which the pitch cycles downward to dive.
- **MaxHeight** (Integer) — default: `200`; range: `50` – `360` — Target altitude to maintain during infinite flight.
- **PitchIncrement** (Decimal) — default: `3.0`; range: `1.0` – `10.0` — Degrees of pitch change per tick during the oscillation cycle.


### Screenshots

*Screenshots for ElytraFly will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleElytraFly.kt)*
