## AutoMobHeal

Automatically heals nearby vanilla-healable mobs using their normal repair or feeding items — for example repairing iron golems with iron ingots, healing tamed wolves and cats with meat, or feeding horses, camels, and nautili. Each mob type can be toggled and tuned individually.

**Category:** World
**Enabled by default:** No

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Range (Decimal | default: 4.5 | range: 1.0..6.0)
├── Delay (Integer Range | default: 4..4 | range: 0..40 | ticks)
├── SlotResetDelay (Integer | default: 2 | range: 0..20 | ticks)
├── SwingMode (Choice | default: DoNotHide | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
└── Mob groups (each a Toggleable Group | default: on)
    ├── IronGolem — HealthThreshold
    ├── Wolf — HealthThreshold, NoWaste
    ├── Cat — HealthThreshold, NoWaste
    ├── HorseFamily — HealthThreshold, NoWaste, AllowGoldenCarrot, AllowGoldenApple, AllowEnchantedGoldenApple
    ├── Camel — HealthThreshold, NoWaste
    └── Nautilus — HealthThreshold, NoWaste, AllowBucketFood
```

### Settings Details

- **Range** (Decimal) — default: `4.5`; range: `1.0` – `6.0` — Maximum distance in blocks to a mob for it to be healed.
- **Delay** (Integer Range) — default: `4` – `4`; range: `0` – `40`; unit: ticks — Delay between heal actions.
- **SlotResetDelay** (Integer) — default: `2`; range: `0` – `20`; unit: ticks — How long to wait before switching back from the food/repair hotbar slot.
- **SwingMode** (Choice) — default: `DoNotHide`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer` — Controls whether the hand-swing animation is shown to you, the server, both, or neither.

#### Mob groups

Each supported mob has its own toggleable group (all enabled by default). They share these settings, plus a few mob-specific ones:

- **HealthThreshold** (Decimal) — default: `75.0`; range: `1.0` – `100.0`; unit: % — Only heal the mob while its health is at or below this percentage.
- **NoWaste** (Toggle) — default: `true` — *(food-eating mobs)* Avoid feeding when it would overheal and waste the item.
- **AllowGoldenCarrot / AllowGoldenApple / AllowEnchantedGoldenApple** (Toggle) — default: `false` — *(HorseFamily only)* Allow using these valuable items to heal horses, donkeys, and mules.
- **AllowBucketFood** (Toggle) — default: `false` — *(Nautilus only)* Allow using bucket-based food (e.g. a bucket of fish) to heal.

### Screenshots

*Screenshots for AutoMobHeal will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2Fautomobheal%2FAutoMobHeal.kt)*
