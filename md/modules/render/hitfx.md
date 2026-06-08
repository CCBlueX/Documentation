## HitFX

HitFX turns a successful hit on another player or mob into a little celebration. Whenever you land an attack, it can spawn particles around your target and play a fun sound effect, so combat feels more rewarding and your hits are easier to register at a glance.

You can pick which particles appear (from blood splatters to fire, hearts, water, smoke, magic sparkles, or crit stars) and how many of them burst out per hit. On top of that, HitFX offers two separate sound pools: one for the sounds played when you hit someone, and a personal one that only plays for you. Mix and match the playful built-in sounds to taste — leave a list empty to skip that part of the effect entirely.

This is purely a cosmetic, client-side feature: it changes what you see and hear, not how your attacks behave. It pairs nicely with other visual touches like [DamageParticles](/docs/modules/render/damageparticles) and [Animations](/docs/modules/render/animations).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Particle | Multi-Select | [Fire] | Blood, Fire, Heart, Water, Smoke, Magic, Crits | Which particle effects can appear when you hit a target. One is picked at random per particle spawned; leave empty for no particles. |
| ParticleAmount | Integer Range | 1..1 | 1..20 | How many particles to spawn per hit. A random value within this range is chosen each time. |
| OtherSound | Multi-Select | [Bonk, Click, Moan, UWU] | Hit, Orb, Bonk, Boykisser, Bring, Glass, Click, Meow, Moan, MagicSquash, NYA, Pop, Soft, Squash, Tung, UWU | Pool of sounds that can play when you hit a target. One sound is chosen at random per hit; leave empty for silence. |
| SelfSound | Multi-Select | [Boykisser] | Hit, Orb, Bonk, Boykisser, Bring, Glass, Click, Meow, Moan, MagicSquash, NYA, Pop, Soft, Squash, Tung, UWU | Personal pool of sounds played just for you on a hit. One is chosen at random; leave empty for none. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/hitfx/ModuleHitFX.kt)*
