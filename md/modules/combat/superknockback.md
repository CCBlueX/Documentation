## SuperKnockback

SuperKnockback makes your hits push enemies further away. In Minecraft, a sprinting hit gives extra knockback, but only once per sprint. This module restarts your sprint around each hit so every hit gets the extra push.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Packet | Packet, SprintTap, WTap | How the sprint is restarted. Packet tells the server you stopped and started sprinting, without changing how you move. SprintTap stops your sprint for a moment after a hit. WTap lets go of the forward key for a moment after a hit, like doing a W-tap yourself. |
| Mode → [SprintTap] → ReSprint | Integer Range | 0..1 | 0..10 ticks | How long to wait before sprinting again, in ticks (20 per second). |
| Mode → [WTap] → UntilMovementBlock | Integer Range | 0..1 | 0..10 ticks | How long to wait after the hit before letting go of forward. |
| Mode → [WTap] → UntilAllowedMovement | Integer Range | 0..1 | 0..10 ticks | How long to stay stopped before walking forward again. |
| HurtTime | Integer | 10 | 0..10 | Only works if the enemy was not hurt more recently than this. Lower values skip enemies that were just hit. |
| Chance | Decimal | 100.0 | 0.0..100.0 % | How often the extra knockback is used on a hit. |
| Conditions | Multi-Select | NotInWater | OnlyFacing, OnlyOnGround, NotInWater | Only works when all picked conditions are true. OnlyFacing: the enemy is looking at you. OnlyOnGround: you are on the ground. NotInWater: you are not in water. |
| OnlyOnMove | Toggleable Group | On | | Only works while you are moving. |
| OnlyOnMove → OnlyForward | Toggle | true | | Does not work while you are walking sideways. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleSuperKnockback.kt)*
