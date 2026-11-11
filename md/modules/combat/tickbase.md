## TickBase

TickBase lets you reach an enemy a little earlier than they expect, so you get the first hit. While an enemy is near but not yet in reach, it slows your game down a tiny bit to save up time. When a hit becomes possible, it spends that saved time to get there faster. It works best together with [KillAura](/docs/modules/combat/killaura).

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Timer | Timer, HoldFirst, BurstFirst | How the saved time is spent. Timer speeds up your game until the hit lands. HoldFirst freezes you for a moment and then jumps ahead all at once. BurstFirst jumps ahead right away and freezes afterwards. |
| Mode → [Timer] → BoostSpeed | Decimal | 5.0 | 1.0..10.0 | How much faster the game runs while speeding up. |
| Mode → [HoldFirst/BurstFirst] → MaxTicks | Integer | 4 | 1..20 ticks | How far you can jump ahead at once, in ticks (20 per second). |
| Mode → [HoldFirst/BurstFirst] → Delay | Integer Range | 0..0 | 0..20 ticks | How long the game runs normally between freezing and jumping ahead. |
| Requires | Multi-Select | KillAura | KillAura, LookingAt, Click, OnGround | Only spends saved time when all picked conditions are true. KillAura: KillAura is on and has a target. LookingAt: your crosshair is on the enemy. Click: you are holding attack. OnGround: you stand on the ground. |
| Chance | Decimal | 100.0 | 0.0..100.0 % | How often TickBase uses a chance to hit early. |
| Cooldown | Integer Range | 0..0 | 0..100 ticks | How long to wait after speeding up before doing it again. |
| AttackCooldown | Decimal | 1.0 | 0.0..1.0 | How charged your attack has to be when the hit lands. 1.0 is fully charged. Only matters on servers with an attack cooldown (1.9 and newer). |
| MaxBalance | Integer | 3 | 0..40 ticks | How much time TickBase saves up at most. |
| ChargeRange | Decimal | 50.0 | 0.0..500.0 | How close an enemy has to be, in blocks, before TickBase starts saving up time. |
| ChargeSpeed | Decimal | 0.9 | 0.1..1.0 | How fast the game runs while saving up. 1.0 is normal speed and saves nothing. |
| ChargeWhileUsingItem | Toggle | false | | Also saves up time while you eat, drink or block. |
| ResetBalanceOnFlag | Toggle | true | | Throws away the saved time when the server pulls you back. |
| Advantage | Toggleable Group | On | | Only hits early when the enemy cannot hit you right back. |
| Advantage → EnemyRange | Decimal | 3.0 | 0.0..8.0 blocks | How far away the enemy has to be pushed by your hit to be out of their reach. |
| Advantage → KnockbackTicks | Integer | 2 | 0..10 ticks | How long after your hit the enemy must not be able to hit back. |
| Advantage → KnockbackMultiplier | Decimal | 1.0 | 0.0..3.0 | How strong knockback is on this server compared to normal Minecraft. |
| Advantage → SkipInvulnerable | Toggle | true | | Does not hit early while the enemy still can't take damage from the last hit. |
| Advantage → EnemyCooldown | Toggle | true | | Also hits early when the enemy's attack is not charged yet. |
| Advantage → Criticals | Toggle | true | | Also hits early when your hit will be a critical hit. |
| Visuals | Toggleable Group | On | | Shows where you will be when the hit lands. |
| Visuals → Color | Color | | | Color of the path and the outline. |
| Visuals → BalanceRing | Toggle | true | | Shows a ring around your feet that fills up with saved time. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleTickBase.kt)*
