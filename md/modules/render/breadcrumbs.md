## Breadcrumbs

Leaves a trace behind you.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── OnlyOwn (Toggle | default: true)
├── Color (Color)
├── Rainbow (Toggle | default: false)
├── Height (Decimal | default: 0.5 | range: 0.0..2.0)
└── Temporary (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── Alive (Integer | default: 900 | range: 10..10000 | ms)
    └── Fade (Toggle | default: true)
```

### Settings Details

- **OnlyOwn** (Toggle) — default: `true` — Only draws a trail behind your own player.
- **Color** (Color) — Color of the trail line or quad.
- **Rainbow** (Toggle) — default: `false` — Uses a cycling rainbow color instead of the static color.
- **Height** (Decimal) — default: `0.5`; range: `0.0` – `2.0` — Vertical height of the trail; zero renders lines instead of quads.
#### Temporary

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables automatic removal of old trail segments.
- **Alive** (Integer) — default: `900`; range: `10` – `10000`; unit: ms — How long each trail segment persists before being removed.
- **Fade** (Toggle) — default: `true` — Gradually fades trail segments as they approach expiration.


### Screenshots

*Screenshots for Breadcrumbs will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleBreadcrumbs.kt)*
