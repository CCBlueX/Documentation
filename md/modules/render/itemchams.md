## ItemChams

Applies visual effects to your held items.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Lightmap (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── BlendColor (Color)
│   ├── Alpha (Integer | default: 95 | range: 1..255)
│   ├── GlowColor (Color)
│   ├── Layers (Integer | default: 3 | range: 1..10)
│   ├── LayerSize (Decimal | default: 1.91 | range: 1.0..5.0)
│   └── Falloff (Decimal | default: 6.83 | range: 0.0..20.0)
└── Shield (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── TintMode (Choice | default: MULTIPLY | options: Override, Multiply)
    └── Tint (Color)
```

### Settings Details

#### Lightmap

A toggleable group of settings (default: enabled). Adds a colored glow to your held item.

- **Enabled** (Toggle) — default: `true`
- **BlendColor** (Color) — Base blend color applied to held items.
- **Alpha** (Integer) — default: `95`; range: `1` – `255` — Overall opacity of the held item.
- **GlowColor** (Color) — Color of the glow effect on held items.
- **Layers** (Integer) — default: `3`; range: `1` – `10` — Number of glow layers rendered around the item.
- **LayerSize** (Decimal) — default: `1.91`; range: `1.0` – `5.0` — Size multiplier for each glow layer.
- **Falloff** (Decimal) — default: `6.83`; range: `0.0` – `20.0` — How quickly the glow fades with distance from the item.

#### Shield

A toggleable group of settings (default: enabled). Recolors your shield.

- **Enabled** (Toggle) — default: `true`
- **TintMode** (Choice) — default: `MULTIPLY`; options: `Override`, `Multiply` — `Override` replaces the shield color with the tint; `Multiply` blends the tint into the existing color.
- **Tint** (Color) — Color used to tint the shield.

### Screenshots

*Screenshots for ItemChams will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleItemChams.kt)*
