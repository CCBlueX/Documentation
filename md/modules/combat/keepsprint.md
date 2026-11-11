## KeepSprint

Normally you stop sprinting and slow down when you hit someone. KeepSprint lets you keep sprinting and keep your speed while you fight.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Motion | Decimal Range | 100.0..100.0 | 0.0..100.0 % | How much of your speed you keep after a hit. 100% means you do not slow down. |
| MotionWhenHurt | Decimal Range | 100.0..100.0 | 0.0..100.0 % | How much of your speed you keep after a hit while you were hurt recently (see HurtTime). |
| HurtTime | Integer Range | 1..10 | 1..10 | If you got hurt this many ticks ago (20 ticks per second), MotionWhenHurt is used instead of Motion. |
| Chance | Decimal | 100.0 | 0.0..100.0 % | How often KeepSprint works on a hit. On the other hits you slow down like normal. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleKeepSprint.kt)*
