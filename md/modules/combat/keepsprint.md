## KeepSprint

In vanilla Minecraft, landing a hit on an enemy briefly stops your sprint, forcing a short recovery before you can sprint again. KeepSprint overrides this behaviour so you maintain your sprinting momentum through attacks, keeping your movement speed consistent during combat engagements.

You can fine-tune how much of your forward motion is preserved both during normal attacks and when your target is actively in their hurt animation. The **HurtTime** range lets you define which hurt-time ticks count as "recently hit" for the purpose of applying the **MotionWhenHurt** value instead of the base **Motion** value. Setting either motion range below 100 % introduces a configurable speed penalty on hits, which can help avoid certain anti-cheat detections. The **Chance** setting adds a further layer of bypass behaviour by randomly skipping the sprint preservation entirely on a per-hit basis.

KeepSprint pairs well with [KillAura](/docs/modules/combat/killaura) and [Criticals](/docs/modules/combat/criticals), since those modules increase your attack rate and the sprint-cancellation penalty would otherwise compound noticeably.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Motion | Decimal Range | 100.0..100.0 | 0.0..100.0 % | Percentage of sprinting motion preserved after hitting an enemy under normal conditions. |
| MotionWhenHurt | Decimal Range | 100.0..100.0 | 0.0..100.0 % | Percentage of sprinting motion preserved when the hit target's hurt timer falls within the HurtTime range. |
| HurtTime | Integer Range | 1..10 | 1..10 | The range of hurt-time ticks during which MotionWhenHurt is applied instead of Motion. |
| Chance | Decimal | 100.0 | 0.0..100.0 % | Probability (per hit) that sprint preservation is applied at all. Values below 100 % cause the module to occasionally skip, which can reduce anti-cheat flags. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleKeepSprint.kt)*
