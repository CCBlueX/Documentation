## Criticals

Automatically deals critical damage every time you attack an entity.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Packet | modes: None, Packet, NoGround, Jump, Blink, Timer)
│   ├── [Mode: Packet]
│   │   ├── Mode (Choice | default: NO_CHEAT_PLUS | options: Vanilla, NoCheatPlus, Falling, Low, Down, Grim, BlocksMC)
│   │   └── PacketType (Choice | default: FULL | options: OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full)
│   ├── [Mode: Jump]
│   │   ├── Height (Decimal | default: 0.42 | range: 0.1..0.42)
│   │   ├── Range (Decimal | default: 4.0 | range: 1.0..6.0)
│   │   ├── OptimizeForCooldown (Toggle | default: true)
│   │   ├── CheckKillaura (Toggle | default: false)
│   │   ├── CheckAutoClicker (Toggle | default: false)
│   │   └── CanBeSeen (Toggle | default: true)
│   ├── [Mode: Blink]
│   │   ├── Delay (Integer Range | default: 300..600 | range: 0..1000 | ms)
│   │   └── Range (Decimal | default: 4.0 | range: 0.0..10.0)
│   └── [Mode: Timer]
│       ├── Speed (Decimal | default: 0.8 | range: 0.1..1.0)
│       └── Range (Decimal | default: 4.0 | range: 0.0..10.0)
├── WhenSprinting (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── StopSprinting (Choice | default: LEGIT | options: None, Legit, OnNetwork, OnAttack)
│   └── Range (Decimal | default: 4.0 | range: 0.0..10.0)
└── Visuals (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── Fake (Toggle | default: false)
    ├── Critical (Integer | default: 1 | range: 0..20)
    └── Magic (Integer | default: 0 | range: 0..20)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **None**, **Packet**, **NoGround**, **Jump**, **Blink**, **Timer**. Default: **Packet**.

##### Mode: Packet

- **Mode** (Choice) — default: `NO_CHEAT_PLUS`; options: `Vanilla`, `NoCheatPlus`, `Falling`, `Low`, `Down`, `Grim`, `BlocksMC` — Selects the packet-based critical hit method for different anti-cheats.
- **PacketType** (Choice) — default: `FULL`; options: `OnGroundOnly`, `PositionAndOnGround`, `LookAndOnGround`, `Full` — Type of movement packet sent to spoof fall distance.

##### Mode: Jump

- **Height** (Decimal) — default: `0.42`; range: `0.1` – `0.42` — Jump height velocity for triggering critical hits (0.42 is a normal jump).
- **Range** (Decimal) — default: `4.0`; range: `1.0` – `6.0` — Detection radius for enemies to trigger auto-jump criticals.
- **OptimizeForCooldown** (Toggle) — default: `true` — Waits for the attack cooldown to maximize damage before jumping.
- **CheckKillaura** (Toggle) — default: `false` — Only activates jump criticals when the KillAura module is running.
- **CheckAutoClicker** (Toggle) — default: `false` — Only activates jump criticals when the AutoClicker module is running.
- **CanBeSeen** (Toggle) — default: `true` — Requires line-of-sight to the enemy before triggering a jump.

##### Mode: Blink

- **Delay** (Integer Range) — default: `300` – `600`; range: `0` – `1000`; unit: ms — Duration to delay packets before releasing to create a fake-lag critical effect.
- **Range** (Decimal) — default: `4.0`; range: `0.0` – `10.0` — Detection radius for enemies to activate blink mode.

##### Mode: Timer

- **Speed** (Decimal) — default: `0.8`; range: `0.1` – `1.0` — Timer speed multiplier that slows game ticks when an enemy is in range.
- **Range** (Decimal) — default: `4.0`; range: `0.0` – `10.0` — Detection radius for enemies to enable timer slowdown.

#### WhenSprinting

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **StopSprinting** (Choice) — default: `LEGIT`; options: `None`, `Legit`, `OnNetwork`, `OnAttack` — Controls when to stop sprinting for critical hits: never, on sprint ticks, on network packets, or on attack.
- **Range** (Decimal) — default: `4.0`; range: `0.0` – `10.0` — Distance to search for enemies before attempting a critical while sprinting.

#### Visuals

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Fake** (Toggle) — default: `false` — Shows critical hit particles even when not dealing actual critical damage.
- **Critical** (Integer) — default: `1`; range: `0` – `20` — Number of critical hit particle effects to display on each attack.
- **Magic** (Integer) — default: `0`; range: `0` – `20` — Number of magic particle effects to display on each attack.


### Screenshots

*Screenshots for Criticals will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleCriticals.kt)*
