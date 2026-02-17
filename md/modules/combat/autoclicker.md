## AutoClicker

Clicks automatically when holding down the attack button.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Attack (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Clicker (Setting Group)
│   │   ├── CPS (Integer Range | default: 5..8 | range: 1..60 | clicks)
│   │   ├── Technique (Choice | default: STABILIZED | options: Stabilized, Efficient, Spamming, DoubleClick, Drag, Butterfly, NormalDistribution)
│   │   ├── ItemCooldown (Setting Group)
│   │   │   └── Minimum (Decimal Range | default: 1.0..1.0 | range: 0.0..2.0)
│   │   └── AttackCooldown (Toggle | default: true)
│   ├── RequiresNoInput (Toggle | default: false)
│   ├── DelayOnBroken (Toggle | default: true)
│   ├── Objective (Choice | default: ANY | options: Enemy, Entity, Block, Any)
│   ├── OnItemUse (Choice | default: WAIT | options: Wait, Stop, Ignore)
│   ├── Weapon (Choice | default: ANY | options: Sword, Axe, Both, Any)
│   ├── Criticals (Choice | default: SMART | options: Smart, Ignore, Always)
│   └── DelayPostStopUse (Integer | default: 0 | range: 0..20 | ticks)
└── Use (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── Clicker (Setting Group)
    │   ├── CPS (Integer Range | default: 5..8 | range: 1..60 | clicks)
    │   └── Technique (Choice | default: STABILIZED | options: Stabilized, Efficient, Spamming, DoubleClick, Drag, Butterfly, NormalDistribution)
    ├── HoldingItemsForIgnore (Registry List)
    ├── BlocksForIgnore (Registry List)
    ├── DelayStart (Toggle | default: false)
    ├── OnlyBlock (Toggle | default: false)
    └── RequiresNoInput (Toggle | default: false)
```

### Settings Details

#### Attack

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### Clicker

> For details on Clicker settings, see [Shared: Clicker](/docs/modules/shared/clicker).

- **RequiresNoInput** (Toggle) — default: `false` — When enabled, attacks trigger without holding the attack key.
- **DelayOnBroken** (Toggle) — default: `true` — Adds a 300ms delay after breaking a block to prevent attack spam.
- **Objective** (Choice) — default: `ANY`; options: `Enemy`, `Entity`, `Block`, `Any` — Determines what type of object triggers automatic clicking.
- **OnItemUse** (Choice) — default: `WAIT`; options: `Wait`, `Stop`, `Ignore` — Controls behavior when an item is being used: wait, stop using, or ignore.
- **Weapon** (Choice) — default: `ANY`; options: `Sword`, `Axe`, `Both`, `Any` — Restricts automatic clicking to specific weapon types held in the main hand.
- **Criticals** (Choice) — default: `SMART`; options: `Smart`, `Ignore`, `Always` — Controls when to wait for critical hit opportunities before attacking.
- **DelayPostStopUse** (Integer) — default: `0`; range: `0` – `20`; unit: ticks — Delay in ticks after stopping item usage before resuming attacks.

#### Use

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
##### Clicker

> For details on Clicker settings, see [Shared: Clicker](/docs/modules/shared/clicker).

- **HoldingItemsForIgnore** (Registry List) — Items that disable clicking when held (e.g., water buckets, ender pearls).
- **BlocksForIgnore** (Registry List) — Blocks that disable clicking when aimed at (e.g., doors, fence gates, trapdoors).
- **DelayStart** (Toggle) — default: `false` — Adds a 2-tick delay on the first use activation.
- **OnlyBlock** (Toggle) — default: `false` — Only clicks when holding block items.
- **RequiresNoInput** (Toggle) — default: `false` — When enabled, use triggers without holding the use key.


### Screenshots

*Screenshots for AutoClicker will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleAutoClicker.kt)*
