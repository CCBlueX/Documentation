## HitFX

HitFX plays particles and a sound when you hit a player or mob, so you can easily tell when a hit landed. Only you see and hear it.

Pick which particles can appear and how many. **OtherSound** is the sound for hitting others and **SelfSound** is the sound for when you get hit. If you pick more than one, a random one plays each time. Leave a list empty to turn that part off. It goes well with [DamageParticles](/docs/modules/render/damageparticles).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Particle | Multi-Select | Fire | Blood, Fire, Heart, Water, Smoke, Magic, Crits | Which particles can appear on a hit. |
| ParticleAmount | Integer Range | 1 to 1 | 1 to 20 | How many particles appear per hit. |
| OtherSound | Multi-Select | Pop | Hit, Orb, Bonk, Boykisser, ApplePay, Aimbooster, Bring, Brick, Bump, Glass, Click, Coin, Meow, Moan, MagicSquash, NYA, OSU, Pop, Soft, Schoolboy, Skeet, Slap, Squash, Tung, TF2 Crit, UWU | Sounds that can play when you hit someone. |
| SelfSound | Multi-Select | Boykisser | Hit, Orb, Bonk, Boykisser, ApplePay, Aimbooster, Bring, Brick, Bump, Glass, Click, Coin, Meow, Moan, MagicSquash, NYA, OSU, Pop, Soft, Schoolboy, Skeet, Slap, Squash, Tung, TF2 Crit, UWU | Sounds that can play when you get hit. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/hitfx/ModuleHitFX.kt)*
