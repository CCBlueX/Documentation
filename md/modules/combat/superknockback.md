## SuperKnockback

Increases knockback dealt to other entities.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Packet | modes: Packet, SprintTap, WTap)
│   ├── [Mode: SprintTap]
│   │   └── ReSprint (Integer Range | default: 0..1 | range: 0..10 | ticks)
│   └── [Mode: WTap]
│       ├── UntilMovementBlock (Integer Range | default: 0..1 | range: 0..10 | ticks)
│       └── UntilAllowedMovement (Integer Range | default: 0..1 | range: 0..10 | ticks)
├── HurtTime (Integer | default: 10 | range: 0..10)
├── Chance (Integer | default: 100 | range: 0..100 | %)
├── Conditions (Multi-Select | default: [NotInWater] | options: OnlyFacing, OnlyOnGround, NotInWater)
└── OnlyOnMove (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    └── OnlyForward (Toggle | default: true)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Packet**, **SprintTap**, **WTap**. Default: **Packet**.

##### Mode: SprintTap

- **ReSprint** (Integer Range) — default: `0` – `1`; range: `0` – `10`; unit: ticks — Ticks to wait before re-sprinting after the sprint tap.

##### Mode: WTap

- **UntilMovementBlock** (Integer Range) — default: `0` – `1`; range: `0` – `10`; unit: ticks — Ticks to wait after attacking before blocking forward movement.
- **UntilAllowedMovement** (Integer Range) — default: `0` – `1`; range: `0` – `10`; unit: ticks — Ticks to wait before allowing movement again after blocking it.

- **HurtTime** (Integer) — default: `10`; range: `0` – `10` — Maximum target hurt-time at which the knockback boost is applied.
- **Chance** (Integer) — default: `100`; range: `0` – `100`; unit: % — Probability that the knockback boost triggers on each attack.
- **Conditions** (Multi-Select) — default: `NotInWater`; options: `OnlyFacing`, `OnlyOnGround`, `NotInWater` — Additional conditions that must be met for the module to operate.
#### OnlyOnMove

A toggleable group of settings (default: enabled). When enabled, only triggers the knockback boost while the player is moving.

- **Enabled** (Toggle) — default: `true` — Enables the movement requirement.
- **OnlyForward** (Toggle) — default: `true` — Restricts the movement requirement to forward movement only.


### Screenshots

*Screenshots for SuperKnockback will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleSuperKnockback.kt)*
