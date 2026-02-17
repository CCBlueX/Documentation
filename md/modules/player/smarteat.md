## SmartEat

Automatically eats food when your hunger is low.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── SwapBackDelay (Integer | default: 5 | range: 1..20)
├── PreferGappleHealthThreshold (Decimal | default: 9.0 | range: 0.0..20.0)
├── PreferNotchAppleHealthThreshold (Decimal | default: 2.0 | range: 0.0..20.0)
├── PreferHealthPotHealthThreshold (Decimal | default: 12.0 | range: 0.0..20.0)
├── CombatPauseTime (Integer | default: 0 | range: 0..40 | ticks)
├── NotDuringCombat (Toggle | default: false)
├── SilentOffhand (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── RenderSlot (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       └── Offset (Integer | default: 40 | range: 30..70)
└── AutoEat (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    └── MinHunger (Integer | default: 15 | range: 0..20)
```

### Settings Details

- **SwapBackDelay** (Integer) — default: `5`; range: `1` – `20` — Ticks to wait before switching back to the original hotbar slot after eating.
- **PreferGappleHealthThreshold** (Decimal) — default: `9.0`; range: `0.0` – `20.0` — Health at or below which golden apples are preferred.
- **PreferNotchAppleHealthThreshold** (Decimal) — default: `2.0`; range: `0.0` – `20.0` — Health at or below which enchanted golden apples are preferred.
- **PreferHealthPotHealthThreshold** (Decimal) — default: `12.0`; range: `0.0` – `20.0` — Health at or below which health potions are preferred.
- **CombatPauseTime** (Integer) — default: `0`; range: `0` – `40`; unit: ticks — Ticks to pause combat actions while eating.
- **NotDuringCombat** (Toggle) — default: `false` — Prevents eating while actively in combat.
#### SilentOffhand

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### RenderSlot

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Offset** (Integer) — default: `40`; range: `30` – `70` — Horizontal pixel offset for the rendered offhand slot indicator.


#### AutoEat

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **MinHunger** (Integer) — default: `15`; range: `0` – `20` — Hunger level below which automatic eating begins.


### Screenshots

*Screenshots for SmartEat will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleSmartEat.kt)*
