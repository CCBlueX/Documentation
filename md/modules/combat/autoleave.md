## AutoLeave

Automatically leaves the server whenever your health goes below the certain threshold.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Health (Decimal | default: 8.0 | range: 0.0..20.0 | HP)
├── Delay (Integer Range | default: 0..0 | range: 0..60 | ticks)
└── Mode (Choice | default: QUIT | options: Quit, InvalidPacket, SelfHurt, IllegalChat, IllegalSwitchitem, IllegalInteract)
```

### Settings Details

- **Health** (Decimal) — default: `8.0`; range: `0.0` – `20.0`; unit: HP — Health threshold below which you will leave the server.
- **Delay** (Integer Range) — default: `0` – `0`; range: `0` – `60`; unit: ticks — Number of consecutive ticks the condition must be met before leaving.
- **Mode** (Choice) — default: `QUIT`; options: `Quit`, `InvalidPacket`, `SelfHurt`, `IllegalChat`, `IllegalSwitchitem`, `IllegalInteract` — Method used to disconnect from the server.

### Screenshots

*Screenshots for AutoLeave will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleAutoLeave.kt)*
