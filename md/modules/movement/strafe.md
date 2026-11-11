## Strafe

Strafe lets you change direction freely while you are in the air. Normally you can barely steer once you jump. With Strafe you can turn sharply mid-jump to dodge hits or go around corners.

The two strength settings work on their own: one for the air and one for the ground. 1.0 gives full control and 0.0 turns that part off. With StrictMovement on, you stop right away in the air when you let go of all movement keys.

It works well with [Speed](/docs/modules/movement/speed) and [LongJump](/docs/modules/movement/longjump).

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| StrengthInAir | Decimal | 1.0 | 0.0..1.0 | How much you can steer in the air. |
| StrengthOnGround | Decimal | 1.0 | 0.0..1.0 | How much it helps you steer on the ground. |
| StrictMovement | Toggle | false | | Stops you right away when you let go of all movement keys. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleStrafe.kt)*
