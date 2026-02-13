## Blink

Makes it look as if you were teleporting to other players.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Dummy (Toggle | default: false)
├── Ambush (Toggle | default: false)
├── AutoDisable (Toggle | default: true)
└── AutoReset (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── ResetAfter (Integer | default: 100 | range: 1..1000)
    └── ResetAction (Choice | default: RESET | options: Reset, Blink)
```

### Settings Details

- **Dummy** (Toggle) — default: `false` — Spawns a fake player clone at your original position.
- **Ambush** (Toggle) — default: `false` — Automatically disables Blink when you interact with an entity.
- **AutoDisable** (Toggle) — default: `true` — Disables the module after an auto reset is triggered.
#### AutoReset

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **ResetAfter** (Integer) — default: `100`; range: `1` – `1000` — Number of queued positions before triggering an automatic reset.
- **ResetAction** (Choice) — default: `RESET`; options: `Reset`, `Blink` — Whether to cancel all packets (Reset) or send them all at once (Blink).


### Screenshots

*Screenshots for Blink will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleBlink.kt)*
