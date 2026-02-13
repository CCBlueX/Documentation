## Particles

Displays particles when attacking an entity.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Size (Decimal | default: 1.0 | range: 0.5..2.0)
├── Count (Integer Range | default: 2..10 | range: 2..30 | particles)
├── RandomParticleRotation (Toggle | default: true)
├── Physical (Setting Group)
│   ├── Motion (Decimal | default: 15.0 | range: 1.0..30.0)
│   ├── BounceX (Decimal | default: 0.8 | range: 0.0..1.0)
│   ├── BounceY (Decimal | default: 0.6 | range: 0.0..1.0)
│   ├── BounceZ (Decimal | default: 0.8 | range: 0.0..1.0)
│   ├── Drag (Decimal | default: 0.99 | range: 0.0..1.0)
│   └── GravityFactor (Decimal | default: 0.8 | range: 0.0..1.0)
├── Color (Color)
└── Particle (Multi-Select | default: [Star] | options: Orbiz, Star, Dollar, Crown, Heart, Lightning, Line, Point, Rhombus, Snowflake, Spark)
```

### Settings Details

- **Size** (Decimal) — default: `1.0`; range: `0.5` – `2.0` — Sets the visual size of each particle.
- **Count** (Integer Range) — default: `2` – `10`; range: `2` – `30`; unit: particles — Sets the number of particles spawned per hit.
- **RandomParticleRotation** (Toggle) — default: `true` — Applies a random rotation to each particle.
#### Physical

A group of related settings.

- **Motion** (Decimal) — default: `15.0`; range: `1.0` – `30.0` — Controls the horizontal speed multiplier of particles.
- **BounceX** (Decimal) — default: `0.8`; range: `0.0` – `1.0` — Sets the velocity retention factor when bouncing on the X axis.
- **BounceY** (Decimal) — default: `0.6`; range: `0.0` – `1.0` — Sets the velocity retention factor when bouncing on the Y axis.
- **BounceZ** (Decimal) — default: `0.8`; range: `0.0` – `1.0` — Sets the velocity retention factor when bouncing on the Z axis.
- **Drag** (Decimal) — default: `0.99`; range: `0.0` – `1.0` — Applies velocity drag on particles when bouncing off surfaces.
- **GravityFactor** (Decimal) — default: `0.8`; range: `0.0` – `1.0` — Scales the gravity effect on particles.

- **Color** (Color) — Sets the color of the particles.
- **Particle** (Multi-Select) — default: `Star`; options: `Orbiz`, `Star`, `Dollar`, `Crown`, `Heart`, `Lightning`, `Line`, `Point`, `Rhombus`, `Snowflake`, `Spark` — Selects which particle textures to use.

### Screenshots

*Screenshots for Particles will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleParticles.kt)*
