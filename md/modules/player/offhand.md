## Offhand

Manages your offhand.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Constraints (Setting Group)
│   ├── StartDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   ├── ClickDelay (Integer Range | default: 2..4 | range: 0..20 | ticks)
│   ├── CloseDelay (Integer Range | default: 1..2 | range: 0..20 | ticks)
│   ├── MissChance (Integer Range | default: 0..0 | range: 0..100 | %)
│   └── Requires (Multi-Select | options: NoMovement, NoRotation, InventoryOpen)
├── SwitchMode (Choice | default: AUTOMATIC | options: Smart, Switch, PickUp, Automatic)
├── SwitchDelay (Integer | default: 0 | range: 0..500 | ms)
├── Cycle (Key)
├── Totem (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── SwitchDelay (Integer | default: 0 | range: 0..500 | ms)
│   ├── SwitchBackDelay (Integer | default: 40 | range: 0..500 | ms)
│   ├── Health (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   ├── HealthThreshold (Integer | default: 14 | range: 0..20)
│   │   ├── Safety (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── SafeHealthThreshold (Integer | default: 10 | range: 0..20)
│   │   ├── SubtractCalculatedDamage (Toggle | default: false)
│   │   ├── PredictExplosionDamageEntities (Toggle | default: true)
│   │   ├── PredictExplosionDamageBlocks (Toggle | default: false)
│   │   ├── MissingArmor (Toggle | default: true)
│   │   ├── PredictFallDamage (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── IgnoreElytra (Toggle | default: false)
│   │   └── SwitchBack (Toggle | default: true)
│   └── SendDirectly (Toggle | default: false)
├── Crystal (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── OnlyWhileCrystalAura (Toggle | default: false)
│   ├── WhenNoTotems (Toggle | default: true)
│   └── CrystalBind (Key)
├── Gapple (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── GappleBind (Key)
│   └── WhileHoldingSword (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       └── OnlyWhileKillAura (Toggle | default: true)
├── StrengthPotion (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── OnlyWhileHoldingSword (Toggle | default: true)
│   ├── OnlyWhileKillAura (Toggle | default: true)
│   └── StrengthBind (Key)
└── Block (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── WhileScaffold (Toggle | default: true)
    └── WhileEagle (Toggle | default: true)
```

### Settings Details

#### Constraints

A group of related settings. *Shared setting group — configured identically across modules that use inventory actions.*

- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **ClickDelay** (Integer Range) — default: `2` – `4`; range: `0` – `20`; unit: ticks
- **CloseDelay** (Integer Range) — default: `1` – `2`; range: `0` – `20`; unit: ticks
- **MissChance** (Integer Range) — default: `0` – `0`; range: `0` – `100`; unit: %
- **Requires** (Multi-Select) — options: `NoMovement`, `NoRotation`, `InventoryOpen`

- **SwitchMode** (Choice) — default: `AUTOMATIC`; options: `Smart`, `Switch`, `PickUp`, `Automatic` — Method used to swap items into the offhand slot.
- **SwitchDelay** (Integer) — default: `0`; range: `0` – `500`; unit: ms — Milliseconds to wait between offhand switches.
- **Cycle** (Key) — Key to cycle through available offhand item types.
#### Totem

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **SwitchDelay** (Integer) — default: `0`; range: `0` – `500`; unit: ms — Milliseconds to wait before switching to a totem.
- **SwitchBackDelay** (Integer) — default: `40`; range: `0` – `500`; unit: ms — Milliseconds to wait before switching back from a totem.
##### Health

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **HealthThreshold** (Integer) — default: `14`; range: `0` – `20` — Health at or below which a totem is equipped.
###### Safety

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **SafeHealthThreshold** (Integer) — default: `10`; range: `0` – `20` — Health threshold when in a safe position like a bedrock hole.

- **SubtractCalculatedDamage** (Toggle) — default: `false` — Subtracts predicted incoming damage from current health for threshold checks.
- **PredictExplosionDamageEntities** (Toggle) — default: `true` — Predicts explosion damage from nearby entities like crystals and creepers.
- **PredictExplosionDamageBlocks** (Toggle) — default: `false` — Predicts explosion damage from beds and respawn anchors.
- **MissingArmor** (Toggle) — default: `true` — Equips a totem if any armor slot is empty.
###### PredictFallDamage

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **IgnoreElytra** (Toggle) — default: `false` — Ignores fall damage prediction while elytra flying.

- **SwitchBack** (Toggle) — default: `true` — Switches back to the previous offhand item when health is safe.

- **SendDirectly** (Toggle) — default: `false` — Bypasses inventory constraints and sends switch packets directly.

#### Crystal

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **OnlyWhileCrystalAura** (Toggle) — default: `false` — Only equips crystals when Crystal Aura is active.
- **WhenNoTotems** (Toggle) — default: `true` — Falls back to crystals when no totems are available.
- **CrystalBind** (Key) — Key to directly switch to crystal mode.

#### Gapple

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **GappleBind** (Key) — Key to directly switch to gapple mode.
##### WhileHoldingSword

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **OnlyWhileKillAura** (Toggle) — default: `true` — Only equips gapple when KillAura is active.


#### StrengthPotion

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **OnlyWhileHoldingSword** (Toggle) — default: `true` — Only equips strength potion when holding a sword.
- **OnlyWhileKillAura** (Toggle) — default: `true` — Only equips strength potion when KillAura is active.
- **StrengthBind** (Key) — Key to directly switch to strength potion mode.

#### Block

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **WhileScaffold** (Toggle) — default: `true` — Equips blocks in offhand while Scaffold is active.
- **WhileEagle** (Toggle) — default: `true` — Equips blocks in offhand while Eagle is active.


### Screenshots

*Screenshots for Offhand will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2Foffhand%2FModuleOffhand.kt)*
