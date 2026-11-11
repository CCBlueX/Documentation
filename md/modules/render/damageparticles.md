## DamageParticles

DamageParticles shows a floating number above a mob or player when its health changes. You see how much damage was done or how much it healed. The numbers float up, grow and fade away.

The colors tell you what happened: a hit, a kill, healing, or healing back to full health.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| TimeToLive | Decimal | 3.0 s | 0.5..5.0 s | How long each number stays. |
| Scale | Decimal | 2.0 | 0.25..4.0 | Size of the numbers. |
| ScaleTransition | Choice | QuadOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the number grows over time. |
| Displacement | Vector3_d | 0, 1.5, 0 | | Where the number moves while it is shown. By default it floats 1.5 blocks up. |
| DisplacementTransition | Choice | QuadOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the number moves over time. |
| TrackMode | Choice | OnTick | OnTick, OnUpdate | OnTick checks health all the time. OnUpdate waits for health updates from the server. |
| Colors → Damage | Color | Red | | Color when something takes damage. |
| Colors → Death | Color | Red | | Color when something dies. |
| Colors → Heal | Color | Green | | Color when something heals. |
| Colors → MaxHealth | Color | Green | | Color when something heals to full health. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleDamageParticles.kt)*
