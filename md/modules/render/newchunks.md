## NewChunks

Highlights chunks that are likely newly generated.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── RenderDistance (Integer | default: 32 | range: 4..128 | chunks)
├── RenderY (Decimal | default: 0.0 | range: -64.0..320.0)
├── AutoY (Toggle | default: false)
├── Smooth (Toggle | default: true)
├── Persist (Toggle | default: true)
├── NewColor (Color)
└── OldColor (Color)
```

### Settings Details

- **RenderDistance** (Integer) — default: `32`; range: `4` – `128`; unit: chunks — Maximum render distance for chunk highlights.
- **RenderY** (Decimal) — default: `0.0`; range: `-64.0` – `320.0` — Y-coordinate at which chunk planes are drawn.
- **AutoY** (Toggle) — default: `false` — Automatically positions the plane 100 blocks below the player.
- **Smooth** (Toggle) — default: `true` — Blends old chunk colors near newly generated chunks.
- **Persist** (Toggle) — default: `true` — Keeps chunk highlights after they are unloaded.
- **NewColor** (Color) — Color for newly generated chunks.
- **OldColor** (Color) — Color for previously existing chunks.

### Screenshots

*Screenshots for NewChunks will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleNewChunks.kt)*
