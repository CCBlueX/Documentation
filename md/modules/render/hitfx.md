## HitFX

Hitting a target triggers a special effect.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Particle (Multi-Select | default: [Fire] | options: Blood, Fire, Heart, Water, Smoke, Magic, Crits)
├── ParticleAmount (Integer Range | default: 1..1 | range: 1..20)
├── OtherSound (Multi-Select | default: [Pop] | options: Hit, Orb, Bonk, Boykisser, Bring, Glass, Click, Meow, Moan, MagicSquash, NYA, Pop, Soft, Squash, Tung, UWU)
└── SelfSound (Multi-Select | default: [Boykisser] | options: Hit, Orb, Bonk, Boykisser, Bring, Glass, Click, Meow, Moan, MagicSquash, NYA, Pop, Soft, Squash, Tung, UWU)
```

### Settings Details

- **Particle** (Multi-Select) — default: `Fire`; options: `Blood`, `Fire`, `Heart`, `Water`, `Smoke`, `Magic`, `Crits` — Particle effects to spawn on hit.
- **ParticleAmount** (Integer Range) — default: `1` – `1`; range: `1` – `20` — Number of particles spawned per hit.
- **OtherSound** (Multi-Select) — default: `Pop`; options: `Hit`, `Orb`, `Bonk`, `Boykisser`, `Bring`, `Glass`, `Click`, `Meow`, `Moan`, `MagicSquash`, `NYA`, `Pop`, `Soft`, `Squash`, `Tung`, `UWU` — Sound played when hitting another entity.
- **SelfSound** (Multi-Select) — default: `Boykisser`; options: `Hit`, `Orb`, `Bonk`, `Boykisser`, `Bring`, `Glass`, `Click`, `Meow`, `Moan`, `MagicSquash`, `NYA`, `Pop`, `Soft`, `Squash`, `Tung`, `UWU` — Sound played when you are hit.

### Screenshots

*Screenshots for HitFX will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2Fhitfx%2FModuleHitFX.kt)*
