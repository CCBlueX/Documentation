## ItemChams

Applies visual effects to your held items.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── BlendColor (Color)
├── Alpha (Integer | default: 95 | range: 1..255)
├── GlowColor (Color)
├── Layers (Integer | default: 3 | range: 1..10)
├── LayerSize (Decimal | default: 1.91 | range: 1.0..5.0)
└── Falloff (Decimal | default: 6.83 | range: 0.0..20.0)
```

### Settings Details

- **BlendColor** (Color) — Base blend color applied to held items.
- **Alpha** (Integer) — default: `95`; range: `1` – `255` — Overall opacity of the held item.
- **GlowColor** (Color) — Color of the glow effect on held items.
- **Layers** (Integer) — default: `3`; range: `1` – `10` — Number of glow layers rendered around the item.
- **LayerSize** (Decimal) — default: `1.91`; range: `1.0` – `5.0` — Size multiplier for each glow layer.
- **Falloff** (Decimal) — default: `6.83`; range: `0.0` – `20.0` — How quickly the glow fades with distance from the item.

### Screenshots

*Screenshots for ItemChams will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleItemChams.kt)*
