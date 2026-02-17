## Rotations

Allows you to see server-sided rotations.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── BodyPart (Multi-Select | default: [Head, Body] | options: Head, Body)
├── Smooth (Decimal | default: 0.0 | range: 0.0..0.3)
├── VectorLine (Color)
└── VectorDot (Color)
```

### Settings Details

- **BodyPart** (Multi-Select) — default: `Head`, `Body`; options: `Head`, `Body` — Selects which body parts display the server-side rotation.
- **Smooth** (Decimal) — default: `0.0`; range: `0.0` – `0.3` — Smooths the visual rotation interpolation.
- **VectorLine** (Color) — Sets the color of the rotation direction line (alpha 0 disables).
- **VectorDot** (Color) — Sets the color of the rotation direction dot (alpha 0 disables).

### Screenshots

*Screenshots for Rotations will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleRotations.kt)*
