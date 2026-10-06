## Strafe

Strafe restores full directional control over your movement while you are in the air. In vanilla Minecraft, air strafing is heavily dampened — you can barely change direction once you leave the ground. With this module enabled, your inputs are applied at full (or configurable) strength mid-air, letting you cut corners, dodge attacks, and reposition precisely while airborne.

Two separate strength sliders let you tune the effect independently for when you are in the air and when you are on the ground. Setting either to `0.0` disables the correction for that phase entirely, while the default of `1.0` gives maximum responsiveness. When **StrictMovement** is on, releasing all movement keys while airborne immediately cancels any leftover horizontal momentum rather than letting your character drift.

Strafe pairs well with modules like [Speed](/docs/modules/movement/speed) or [LongJump](/docs/modules/movement/longjump) where precise mid-air direction changes are important. It is also useful in PvP to strafe around opponents without losing speed after jumps.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| StrengthInAir | Decimal | 1.0 | 0.0 – 1.0 | How strongly your directional inputs are applied while you are airborne. Lower values reduce air control; 0.0 disables in-air strafing entirely. |
| StrengthOnGround | Decimal | 1.0 | 0.0 – 1.0 | How strongly your directional inputs are applied while you are on the ground. Lower values reduce ground strafing; 0.0 disables it entirely. |
| StrictMovement | Toggle | true | — | When enabled, releasing all movement keys immediately zeroes out your horizontal velocity, preventing any unwanted drift. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleStrafe.kt)*
