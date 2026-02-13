## Timer

Changes the speed the game is running at.

**Category:** World  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: Classic | modes: Classic, Pulse, Boost)
    ├── [Mode: Classic]
    │   └── Speed (Decimal | default: 2.0 | range: 0.1..20.0)
    ├── [Mode: Pulse]
    │   ├── NormalSpeed (Decimal | default: 0.5 | range: 0.1..20.0)
    │   ├── NormalSpeedTicks (Integer | default: 20 | range: 1..500 | ticks)
    │   ├── BoostSpeed (Decimal | default: 2.0 | range: 0.1..20.0)
    │   ├── BoostSpeedTicks (Integer | default: 20 | range: 1..500 | ticks)
    │   └── OnMove (Toggle | default: false)
    └── [Mode: Boost]
        ├── BoostSpeed (Decimal | default: 1.3 | range: 0.1..20.0)
        ├── SlowSpeed (Decimal | default: 0.6 | range: 0.1..20.0)
        ├── TimeBoostTicks (Integer | default: 12 | range: 1..60 | ticks)
        ├── AccountTimerValues (Toggle | default: true)
        ├── NormalizeDuringCombat (Toggle | default: true)
        └── AllowNegative (Toggle | default: false)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Classic**, **Pulse**, **Boost**. Default: **Classic**.

##### Mode: Classic

- **Speed** (Decimal) — default: `2.0`; range: `0.1` – `20.0`

##### Mode: Pulse

- **NormalSpeed** (Decimal) — default: `0.5`; range: `0.1` – `20.0`
- **NormalSpeedTicks** (Integer) — default: `20`; range: `1` – `500`; unit: ticks
- **BoostSpeed** (Decimal) — default: `2.0`; range: `0.1` – `20.0`
- **BoostSpeedTicks** (Integer) — default: `20`; range: `1` – `500`; unit: ticks
- **OnMove** (Toggle) — default: `false`

##### Mode: Boost

- **BoostSpeed** (Decimal) — default: `1.3`; range: `0.1` – `20.0`
- **SlowSpeed** (Decimal) — default: `0.6`; range: `0.1` – `20.0`
- **TimeBoostTicks** (Integer) — default: `12`; range: `1` – `60`; unit: ticks
- **AccountTimerValues** (Toggle) — default: `true`
- **NormalizeDuringCombat** (Toggle) — default: `true`
- **AllowNegative** (Toggle) — default: `false`


### Screenshots

*Screenshots for Timer will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2FModuleTimer.kt)*
