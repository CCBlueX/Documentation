## ProphuntESP

Shows you props in Prophunt.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Tracking (Multi-Select | default: [FallingBlocks, BlockUpdates, ChunkDeltaUpdates] | options: FallingBlocks, BlockUpdates, ChunkDeltaUpdates)
└── RenderBlockUpdates (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── Clump (Toggle | default: true)
    ├── StartSize (Decimal | default: 1.0 | range: 0.0..2.0)
    ├── StartCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── EndSize (Decimal | default: 0.8 | range: 0.0..2.0)
    ├── EndCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── FadeInCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── FadeOutCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── InTime (Integer | default: 500 | range: 0..5000 | ms)
    ├── OutTime (Integer | default: 500 | range: 0..5000 | ms)
    ├── Color (Color)
    └── OutlineColor (Color)
```

### Settings Details

- **Tracking** (Multi-Select) — default: `FallingBlocks`, `BlockUpdates`, `ChunkDeltaUpdates`; options: `FallingBlocks`, `BlockUpdates`, `ChunkDeltaUpdates`
#### RenderBlockUpdates

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Clump** (Toggle) — default: `true`
- **StartSize** (Decimal) — default: `1.0`; range: `0.0` – `2.0`
- **StartCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **EndSize** (Decimal) — default: `0.8`; range: `0.0` – `2.0`
- **EndCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **FadeInCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **FadeOutCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **InTime** (Integer) — default: `500`; range: `0` – `5000`; unit: ms
- **OutTime** (Integer) — default: `500`; range: `0` – `5000`; unit: ms
- **Color** (Color)
- **OutlineColor** (Color)


### Screenshots

*Screenshots for ProphuntESP will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleProphuntESP.kt)*
