## AutoFish

Automatically catches fish when using a rod.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── ReelDelay (Integer Range | default: 5..8 | range: 0..20 | ticks)
├── Sounds (Registry List)
├── SoundDistance (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── MaxDistance (Decimal | default: 1.0 | range: 0.0..10.0 | blocks)
└── RecastRod (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    └── Delay (Integer Range | default: 15..20 | range: 10..30 | ticks)
```

### Settings Details

- **ReelDelay** (Integer Range) — default: `5` – `8`; range: `0` – `20`; unit: ticks — Ticks to wait before reeling in the rod after a bite.
- **Sounds** (Registry List) — Sound events that trigger the pull (default: fishing bobber splash).
#### SoundDistance

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **MaxDistance** (Decimal) — default: `1.0`; range: `0.0` – `10.0`; unit: blocks — Maximum distance between the fishing hook and the trigger sound to count as a valid bite.

#### RecastRod

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Delay** (Integer Range) — default: `15` – `20`; range: `10` – `30`; unit: ticks — Ticks to wait before recasting the rod after reeling in.


### Screenshots

*Screenshots for AutoFish will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleAutoFish.kt)*
