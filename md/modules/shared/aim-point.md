## AimPoint

The AimPoint setting group decides **which exact point on the target** a combat module aims at, and adds optional humanization so the aim does not look perfectly robotic. It is shared by the combat aim modules, so the point-selection behaviour is configured the same way everywhere.

The AimPoint setting group appears in the following modules:
- [Aimbot](/docs/modules/combat/aimbot)
- [KillAura](/docs/modules/combat/killaura)
- [AutoRod](/docs/modules/combat/autorod)
- [AutoShoot](/docs/modules/combat/autoshoot)

By default the module searches the target's hitbox for the easiest point to hit. The settings below let you restrict that search and add random, human-like wobble.

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| ExemptBoxParts | Multi-Select | [] | Head, Body, Feet | Hitbox parts that are never aimed at (e.g. exclude Head to avoid headshots). |
| ExemptBestHitVector | Toggleable Group | off | — | Use a fixed offset from the hitbox instead of searching for the easiest-to-hit point. |
| ExemptBestHitVector → Vertical | Decimal | 0.2 | 0.0..1.0 | Vertical position within the hitbox used for the fixed point. |
| ExemptBestHitVector → Horizontal | Decimal | 0.1 | 0.0..1.0 | Horizontal position within the hitbox used for the fixed point. |
| Gaussian | Toggleable Group | off | — | Adds a smooth, gaussian-random wobble to the aim point to look more human. |
| Gaussian → YawOffset | Decimal Range | 0.0..0.0 | 0.0..1.0 | Random horizontal offset range. |
| Gaussian → PitchOffset | Decimal Range | 0.0..0.0 | 0.0..1.0 | Random vertical offset range. |
| Gaussian → Chance | Integer | 100 | 0..100 % | Chance that the wobble is applied. |
| Gaussian → Speed | Decimal Range | 0.1..0.2 | 0.01..1.0 | How fast the wobble moves toward its target offset. |
| Gaussian → Tolerance | Decimal | 0.05 | 0.01..0.1 | Distance at which the offset counts as reached. |
| Gaussian → Dynamic | Toggleable Group | off | — | Scales the wobble by the target's hurt time and distance. |
| Gaussian → Dynamic → HurtTime | Integer | 10 | 0..10 | Target hurt-time used in the scaling. |
| Gaussian → Dynamic → YawFactor | Decimal | 0.0 | 0.0..10.0 × | Multiplier applied to the horizontal wobble. |
| Gaussian → Dynamic → PitchFactor | Decimal | 0.0 | 0.0..10.0 × | Multiplier applied to the vertical wobble. |
| Gaussian → Dynamic → Speed | Decimal Range | 0.5..0.75 | 0.01..1.0 | Wobble speed while dynamic scaling is active. |
| Gaussian → Dynamic → Tolerance | Decimal | 0.1 | 0.01..0.1 | Reach tolerance while dynamic scaling is active. |
| Lazy | Toggleable Group | off | — | Only re-picks the aim point once it has drifted past a threshold (reduces jitter). |
| Lazy → Threshold | Decimal Range | 0.1..0.2 | 0.01..0.4 m | Drift distance before the aim point is recomputed. |
| Delay | Toggleable Group | off | — | Waits before moving to a newly chosen aim point. |
| Delay → Delay | Integer Range | 2..4 | 0..5 ticks | Ticks to wait before switching aim point. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Futils%2Faiming%2Fpoint%2FPointTracker.kt)*
