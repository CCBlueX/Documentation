## Aimbot

Aimbot quietly turns your view toward nearby players and mobs so your crosshair tracks them for you. It only aims — it does not click or attack — so it pairs well with a manual playstyle or with modules that handle the clicking, like [AutoClicker](/docs/modules/combat/autoclicker) or [KillAura](/docs/modules/combat/killaura).

You choose how far it reaches, who it locks onto, and how the aim point is picked, then tune how the turn feels with the AngleSmooth modes. Smoother, slower settings look more human; faster settings snap on more aggressively. You can also limit it to only the horizontal or vertical part of the aim, and decide whether it should keep aiming while you have a screen or container open.

The Requires options let you gate the assist behind conditions — for example, only while clicking, only while holding a weapon, or only while not breaking a block — so it engages exactly when you want it and stays idle the rest of the time.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 4.2 | 1.0..8.0 | How close a target must be, in blocks, before Aimbot will face it. |
| Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |
| TargetRendering | Toggleable Group | On | — | See [Shared: TargetRendering](/docs/modules/shared-settings/target-rendering). |
| AimPoint | Setting Group | — | — | See [Shared: AimPoint](/docs/modules/shared-settings/aim-point). |
| Requires | Multi-Select | [Click] | options: Click, Weapon, EmptyHand, VanillaName, NotBreaking | Conditions that must all be true for Aimbot to engage — for example only while clicking, holding a weapon, with an empty hand, using a vanilla item name, or while not breaking a block. |
| AngleSmooth | Mode Selector | Linear | modes: Interpolation, Sigmoid, Linear | How the turn toward the target is smoothed out to make it look more natural. |
| AngleSmooth → [Interpolation] → HorizontalSpeed | Integer Range | 80..85 | 1..100 (%) | Portion of the remaining horizontal angle closed each tick. |
| AngleSmooth → [Interpolation] → VerticalSpeed | Integer Range | 20..25 | 1..100 (%) | Portion of the remaining vertical angle closed each tick. |
| AngleSmooth → [Interpolation] → DirectionChangeFactor | Integer Range | 95..100 | 0..100 (%) | How readily the aim reverses direction when the target moves the other way. |
| AngleSmooth → [Interpolation] → Midpoint | Decimal | 0.35 | 0.0..1.0 | Where the fastest part of the turn falls along the path to the target. |
| AngleSmooth → [Sigmoid] → HorizontalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | Maximum horizontal turn speed, in degrees, for the S-curve motion. |
| AngleSmooth → [Sigmoid] → VerticalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | Maximum vertical turn speed, in degrees, for the S-curve motion. |
| AngleSmooth → [Sigmoid] → Steepness | Decimal | 10.0 | 0.0..20.0 | How sharply the turn accelerates and decelerates across the curve. |
| AngleSmooth → [Sigmoid] → Midpoint | Decimal | 0.3 | 0.0..1.0 | Where the fastest part of the turn falls along the path to the target. |
| AngleSmooth → [Linear] → HorizontalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | Maximum horizontal turn speed, in degrees, at a steady rate. |
| AngleSmooth → [Linear] → VerticalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | Maximum vertical turn speed, in degrees, at a steady rate. |
| Axis | Multi-Select | [Vertical] | options: Horizontal, Vertical | Which parts of your aim Aimbot is allowed to control — horizontal (yaw), vertical (pitch), or both. |
| Ignore | Multi-Select | [] | options: Screen, Container | Open screens that Aimbot should keep aiming through instead of stopping — any screen, or container/inventory screens specifically. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAimbot.kt)*
