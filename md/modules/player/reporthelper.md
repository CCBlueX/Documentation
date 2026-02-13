## ReportHelper

Automatically starts a report and confirms it for you.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── AutoReport (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── Delay (Integer Range | default: 1..3 | range: 0..20 | ticks)
│   ├── Chance (Integer | default: 100 | range: 1..100 | %)
│   └── CommandPattern (Text)
└── AutoConfirm (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    └── Mode (Mode Selector | default: Hypixel | modes: Hypixel, Heypixel)
```

### Settings Details

#### AutoReport

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Delay** (Integer Range) — default: `1` – `3`; range: `0` – `20`; unit: ticks — Ticks to wait before sending the report command.
- **Chance** (Integer) — default: `100`; range: `1` – `100`; unit: % — Probability of actually reporting a detected player.
- **CommandPattern** (Text) — The command template used to report a player, with %s as the player name placeholder.

#### AutoConfirm

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
##### Mode

Select a mode for this feature. Available modes: **Hypixel**, **Heypixel**. Default: **Hypixel**.



### Screenshots

*Screenshots for ReportHelper will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2Freporthelper%2FModuleReportHelper.kt)*
