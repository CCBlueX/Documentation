## AutoShop

Automatically buys specific items in a BedWars shop.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Config (Choice | default: PIKA_NETWORK | options: PikaNetwork, BlocksMC, CubeCraft, TeamHoly, FunnyMC, Dexland)
├── StartDelay (Integer Range | default: 1..2 | range: 0..10 | ticks)
├── PurchaseMode (Mode Selector | default: Normal | modes: Normal, Quick)
│   ├── [Mode: Normal]
│   │   └── ExtraDelay (Integer Range | default: 2..3 | range: 0..10 | ticks)
│   └── [Mode: Quick]
│       ├── Delay (Integer Range | default: 50..70 | range: 0..150 | ms)
│       └── WaitForItems (Toggle | default: true)
├── ExtraCategorySwitchDelay (Integer Range | default: 3..4 | range: 0..10 | ticks)
└── AutoClose (Toggle | default: true)
```

### Settings Details

- **Config** (Choice) — default: `PIKA_NETWORK`; options: `PikaNetwork`, `BlocksMC`, `CubeCraft`, `TeamHoly`, `FunnyMC`, `Dexland` — Preset shop configuration for the target server.
- **StartDelay** (Integer Range) — default: `1` – `2`; range: `0` – `10`; unit: ticks — Ticks to wait after opening the shop before the first click.
#### PurchaseMode

Select a mode for this feature. Available modes: **Normal**, **Quick**. Default: **Normal**.

##### Mode: Normal

- **ExtraDelay** (Integer Range) — default: `2` – `3`; range: `0` – `10`; unit: ticks — Extra ticks to wait after each item purchase.

##### Mode: Quick

- **Delay** (Integer Range) — default: `50` – `70`; range: `0` – `150`; unit: ms — Milliseconds to wait between clicks in quick purchase mode.
- **WaitForItems** (Toggle) — default: `true` — Waits for items to arrive in inventory before continuing.

- **ExtraCategorySwitchDelay** (Integer Range) — default: `3` – `4`; range: `0` – `10`; unit: ticks — Extra ticks to wait after switching item categories.
- **AutoClose** (Toggle) — default: `true` — Automatically closes the shop after all purchases are complete.

### Screenshots

*Screenshots for AutoShop will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2Fautoshop%2FModuleAutoShop.kt)*
