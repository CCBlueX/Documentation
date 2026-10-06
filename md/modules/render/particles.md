## Particles

Particles adds a visual flair to your attacks by spawning decorative 2D shapes at the point of impact each time you hit an entity. The particles fly outward, obey gravity, bounce off solid blocks, and then gradually fade away — giving your combat a stylised, eye-catching look without affecting gameplay mechanics.

You can choose any combination of eleven particle shapes (stars, hearts, lightning bolts, and more), tune how many spawn per hit, set their size and colour, and control exactly how they move and bounce through the world. Because the effect is purely cosmetic and rendered client-side only, it has no impact on server-side behaviour or performance beyond your own frame rate.

Particles work well alongside other visual combat modules such as [HitFX](/docs/modules/render/hitfx) and [DamageParticles](/docs/modules/render/damageparticles) if you want a richer hit-feedback experience.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Size | Decimal | 1.0 | 0.5 – 2.0 | Controls the base size of each particle. Higher values produce larger shapes. |
| Count | Integer Range | 2..10 | 2..30 particles | The random range for how many particles are spawned per hit. A value is picked randomly within this range on each attack. |
| RandomParticleRotation | Toggle | true | — | When enabled, each particle is assigned a random initial rotation angle. When disabled, all particles face the same fixed direction. |
| Physical → Motion | Decimal | 15.0 | 1.0 – 30.0 | Multiplier applied to horizontal velocity when particles move. Higher values make particles shoot out faster and travel further. |
| Physical → BounceX | Decimal | 0.8 | 0.0 – 1.0 | Fraction of horizontal (X-axis) velocity retained after bouncing off a block face. 1.0 means a perfect elastic bounce; 0.0 stops the particle dead. |
| Physical → BounceY | Decimal | 0.6 | 0.0 – 1.0 | Fraction of vertical (Y-axis) velocity retained after bouncing off a floor or ceiling. |
| Physical → BounceZ | Decimal | 0.8 | 0.0 – 1.0 | Fraction of horizontal (Z-axis) velocity retained after bouncing off a block face. |
| Physical → Drag | Decimal | 0.99 | 0.0 – 1.0 | Velocity multiplier applied to horizontal movement on each tick after a ground collision. Values below 1.0 cause particles to slow down as they slide. |
| Physical → GravityFactor | Decimal | 0.8 | 0.0 – 1.0 | Controls how strongly gravity pulls particles downward each tick. 0.0 makes particles float; 1.0 applies maximum gravitational pull. |
| Color | Color | — | — | Tint colour applied to all spawned particles. The colour's alpha channel also controls opacity. |
| Particle | Multi-Select | Star | Orbiz, Star, Dollar, Crown, Heart, Lightning, Line, Point, Rhombus, Snowflake, Spark | One or more particle shapes to use. When multiple shapes are selected, each spawned particle picks one at random from your selection. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleParticles.kt)*
