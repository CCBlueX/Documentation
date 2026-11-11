## AimPoint

The AimPoint settings decide which spot on the enemy you aim at. Normally the module picks the spot that is easiest to hit. You can also make the aim shake a little so it looks more like a real player.

Used by: [Aimbot](/docs/modules/combat/aimbot), [KillAura](/docs/modules/combat/killaura), [AutoRod](/docs/modules/combat/autorod), [AutoShoot](/docs/modules/combat/autoshoot).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ExemptBoxParts | Multi-Select | | Head, Body, Feet | Parts of the enemy that are never aimed at. |
| ExemptBestHitVector | Toggleable Group | Off | | Always aims at a fixed spot on the enemy instead of the easiest one. |
| ExemptBestHitVector → Vertical | Decimal | 0.2 | 0.0..1.0 | How high on the enemy the spot is. 0 is the feet, 1 is the top of the head. |
| ExemptBestHitVector → Horizontal | Decimal | 0.1 | 0.0..1.0 | How far to the side the spot is. |
| Gaussian | Toggleable Group | Off | | Makes the aim spot move around a little at random. |
| Gaussian → YawOffset | Decimal Range | 0.0..0.0 | 0.0..1.0 | How far the spot can move left and right. |
| Gaussian → PitchOffset | Decimal Range | 0.0..0.0 | 0.0..1.0 | How far the spot can move up and down. |
| Gaussian → Chance | Decimal | 100.0 | 0.0..100.0 % | How often the spot moves. |
| Gaussian → Speed | Decimal Range | 0.1..0.2 | 0.01..1.0 | How fast the spot moves. |
| Gaussian → Tolerance | Decimal | 0.05 | 0.01..0.1 | How close the spot has to get to where it is going before it picks a new place. |
| Gaussian → Dynamic | Toggleable Group | Off | | Moves the spot more or less depending on how far away the enemy is and whether it was just hit. |
| Gaussian → Dynamic → HurtTime | Integer | 10 | 0..10 | Only works when the enemy was hit this recently or less. |
| Gaussian → Dynamic → YawFactor | Decimal | 0.0 | 0.0..10.0 x | How much more the spot moves left and right. |
| Gaussian → Dynamic → PitchFactor | Decimal | 0.0 | 0.0..10.0 x | How much more the spot moves up and down. |
| Gaussian → Dynamic → Speed | Decimal Range | 0.5..0.75 | 0.01..1.0 | How fast the spot moves. |
| Gaussian → Dynamic → Tolerance | Decimal | 0.1 | 0.01..0.1 | How close the spot has to get before it picks a new place. |
| Lazy | Toggleable Group | Off | | Keeps aiming at the same spot until the best spot is far enough away. This makes the aim shake less. |
| Lazy → Threshold | Decimal Range | 0.1..0.2 | 0.01..0.4 m | How far away the best spot has to be before the aim moves to it. |
| Delay | Toggleable Group | Off | | Waits a moment before aiming at a new spot. |
| Delay → Delay | Integer Range | 2..4 | 0..5 ticks | How long to wait, in ticks (20 per second). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/aiming/point/PointTracker.kt)*
