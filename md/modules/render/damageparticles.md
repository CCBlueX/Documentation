## DamageParticles

Show health changes of entities.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── TimeToLive (Decimal | default: 3.0 | range: 0.5..5.0 | s)
├── Scale (Decimal | default: 2.0 | range: 0.25..4.0)
├── ScaleTransition (Choice | default: QUAD_OUT | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
├── Displacement (3D Position)
├── DisplacementTransition (Choice | default: QUAD_OUT | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
├── TrackMode (Choice | default: ON_TICK | options: OnTick, OnUpdate)
└── Colors (Setting Group)
    ├── Damage (Color)
    ├── Death (Color)
    ├── Heal (Color)
    └── MaxHealth (Color)
```

### Settings Details

- **TimeToLive** (Decimal) — default: `3.0`; range: `0.5` – `5.0`; unit: s — How long each damage particle remains visible.
- **Scale** (Decimal) — default: `2.0`; range: `0.25` – `4.0` — Size of the damage particle text.
- **ScaleTransition** (Choice) — default: `QUAD_OUT`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None` — Easing function applied to the scale over the particle's lifetime.
- **Displacement** (3D Position) — Direction and distance the particle drifts from its spawn point.
- **DisplacementTransition** (Choice) — default: `QUAD_OUT`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None` — Easing function applied to the displacement over the particle's lifetime.
- **TrackMode** (Choice) — default: `ON_TICK`; options: `OnTick`, `OnUpdate` — When to detect health changes: per game tick or per entity update event.
#### Colors

A group of related settings.

- **Damage** (Color) — Color for damage particles when an entity loses health.
- **Death** (Color) — Color for particles when an entity dies.
- **Heal** (Color) — Color for particles when an entity regains health.
- **MaxHealth** (Color) — Color for particles when an entity reaches maximum health.


### Screenshots

*Screenshots for DamageParticles will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleDamageParticles.kt)*
