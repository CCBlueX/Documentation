## Particles

Particles throws small shapes like stars or hearts out of an entity every time you hit it. They fly away, fall, bounce off blocks and fade out. Only you can see them.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Size | Decimal | 1.0 | 0.5 to 2.0 | How big each particle is. |
| Count | Integer Range | 2..10 | 2..30 particles | How many particles appear per hit. A random number in this range is picked each time. |
| RandomParticleRotation | Toggle | true | | Turns each particle a random way. When off, they all face the same way. |
| Physical → Motion | Decimal | 15.0 | 1.0 to 30.0 | How fast the particles fly away from the hit. |
| Physical → BounceX | Decimal | 0.8 | 0.0 to 1.0 | How much sideways speed (east and west) a particle keeps after hitting a wall. 0 stops it. |
| Physical → BounceY | Decimal | 0.6 | 0.0 to 1.0 | How much up and down speed a particle keeps after hitting the floor or ceiling. |
| Physical → BounceZ | Decimal | 0.8 | 0.0 to 1.0 | How much sideways speed (north and south) a particle keeps after hitting a wall. |
| Physical → Drag | Decimal | 0.99 | 0.0 to 1.0 | How much speed a particle keeps while sliding on the ground. Lower values stop it sooner. |
| Physical → GravityFactor | Decimal | 0.8 | 0.0 to 1.0 | How strongly particles fall. 0 makes them float. |
| Color | Color | | | Color of the particles. The alpha value sets how see-through they are. |
| Particle | Multi-Select | Star | Orbiz, Star, Dollar, Crown, Heart, Lightning, Line, Point, Rhombus, Snowflake, Spark | Which shapes to use. With more than one picked, each particle gets a random one. At least one must stay on. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleParticles.kt)*
