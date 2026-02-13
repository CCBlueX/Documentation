## FastUse

Allows you to use items faster.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Immediate | modes: Immediate, ItemUseTime)
│   ├── [Mode: Immediate]
│   │   ├── Delay (Integer | default: 0 | range: 0..10 | ticks)
│   │   ├── Timer (Decimal | default: 1.0 | range: 0.1..5.0)
│   │   └── Speed (Integer | default: 20 | range: 1..35 | packets)
│   └── [Mode: ItemUseTime]
│       ├── ConsumeTime (Integer | default: 15 | range: 0..20)
│       └── Speed (Integer | default: 20 | range: 1..35 | packets)
├── Conditions (Multi-Select | default: [NotInTheAir] | options: NotInTheAir, NotDuringMove, NotDuringRegeneration)
├── StopInput (Toggle | default: false)
└── PacketType (Choice | default: FULL | options: OnGroundOnly, PositionAndOnGround, LookAndOnGround, Full)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Immediate**, **ItemUseTime**. Default: **Immediate**.

##### Mode: Immediate

- **Delay** (Integer) — default: `0`; range: `0` – `10`; unit: ticks — Ticks to wait before sending speed-up packets.
- **Timer** (Decimal) — default: `1.0`; range: `0.1` – `5.0` — Timer speed multiplier applied during item use.
- **Speed** (Integer) — default: `20`; range: `1` – `35`; unit: packets — Number of movement packets sent per tick to simulate faster eating.

##### Mode: ItemUseTime

- **ConsumeTime** (Integer) — default: `15`; range: `0` – `20` — Ticks the item must be used before triggering fast consume.
- **Speed** (Integer) — default: `20`; range: `1` – `35`; unit: packets — Number of movement packets sent per tick to simulate faster eating.

- **Conditions** (Multi-Select) — default: `NotInTheAir`; options: `NotInTheAir`, `NotDuringMove`, `NotDuringRegeneration` — Conditions that prevent fast use from activating.
- **StopInput** (Toggle) — default: `false` — Stops all movement input while using an item.
- **PacketType** (Choice) — default: `FULL`; options: `OnGroundOnly`, `PositionAndOnGround`, `LookAndOnGround`, `Full` — Type of movement packet sent to speed up item consumption.

### Screenshots

*Screenshots for FastUse will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleFastUse.kt)*
