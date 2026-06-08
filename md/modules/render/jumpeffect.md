## JumpEffect

Shows an effect beneath your feet when jumping.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── EndRadius (Decimal Range | default: 0.15..0.8 | range: 0.0..3.0)
├── InnerColor (Color)
├── OuterColor (Color)
├── AnimCurve (Choice | default: QUAD_OUT | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
├── HueOffsetAnim (Integer | default: 63 | range: -360..360)
├── Lifetime (Integer | default: 15 | range: 1..30)
└── CanBeCovered (Toggle | default: false)
```

### Settings Details

- **EndRadius** (Decimal Range) — default: `0.15` – `0.8`; range: `0.0` – `3.0` — Inner and outer radius of the circle at full expansion.
- **InnerColor** (Color) — Color at the center of the jump circle.
- **OuterColor** (Color) — Color at the outer edge of the jump circle.
- **AnimCurve** (Choice) — default: `QUAD_OUT`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None` — Easing function for the expansion animation.
- **HueOffsetAnim** (Integer) — default: `63`; range: `-360` – `360` — Hue shift applied over the animation lifetime.
- **Lifetime** (Integer) — default: `15`; range: `1` – `30` — Duration in ticks before the circle fades away.
- **CanBeCovered** (Toggle) — default: `false` — When enabled, the effect can be hidden behind blocks; when disabled it is drawn through walls.

### Screenshots

*Screenshots for JumpEffect will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleJumpEffect.kt)*
