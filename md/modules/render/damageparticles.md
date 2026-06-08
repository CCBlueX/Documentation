## DamageParticles

DamageParticles pops up floating numbers above entities whenever their health changes, so you can see exactly how much damage you (or anything else) just dealt or how much an entity healed. Each number rises off the entity, grows, and fades out after a short while, giving you quick visual feedback during fights without staring at health bars.

The numbers are color-coded so you can tell at a glance what happened: a normal hit, a killing blow, a heal, or a heal that tops the entity back up to full health. You can tune how long the numbers stay, how big they get, how they animate, and which colors are used.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| TimeToLive | Decimal | 1.5 | 0.5–5.0 s | How long each number stays on screen before fading out. |
| Scale | Decimal | 1.5 | 0.25–4.0 | Overall size of the floating numbers. |
| ScaleTransition | Choice | QuadOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | Easing curve used to animate the number's size over its lifetime. |
| Displacement | Vector3_d | — | — | Direction and distance the number drifts as it ages (by default it floats upward). |
| DisplacementTransition | Choice | QuadOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | Easing curve used to animate the number's drift over its lifetime. |
| TrackMode | Choice | OnUpdate | OnTick, OnUpdate | When health changes are detected — OnUpdate reacts to server health packets, while OnTick checks entities each game tick. |
| Colors | Setting Group | — | — | Colors used for each type of health change. |
| Colors → Damage | Color | — | — | Color for numbers shown when an entity takes damage. |
| Colors → Death | Color | — | — | Color for numbers shown when an entity is killed. |
| Colors → Heal | Color | — | — | Color for numbers shown when an entity heals. |
| Colors → MaxHealth | Color | — | — | Color for numbers shown when an entity heals back to full health. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleDamageParticles.kt)*
