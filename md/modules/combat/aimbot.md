## Aimbot

Aimbot turns your view toward the closest enemy in front of you, so your crosshair follows them. It only aims and does not attack. You still click yourself, or let a module like [AutoClicker](/docs/modules/combat/autoclicker) click for you.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 4.2 | 1.0..8.0 | How close an enemy has to be, in blocks. |
| WallRange | Decimal | 0.0 | 0.0..8.0 | How close an enemy behind a wall has to be, in blocks. At 0, Aimbot does not aim through walls. It cannot be higher than Range. |
| Target | Setting Group |  | | See [Shared: Target](/docs/modules/shared-settings/target). |
| TargetRendering | Toggleable Group | On | | See [Shared: TargetRendering](/docs/modules/shared-settings/targetrendering). |
| AimPoint | Setting Group |  | | See [Shared: AimPoint](/docs/modules/shared-settings/aimpoint). |
| LazyRotation | Toggle | false | | If your crosshair is already on an enemy, Aimbot does not move it. |
| Crystals | Toggleable Group | Off | | Aims at end crystals in range before enemies. It picks the crystal closest to your crosshair. |
| Crystals → Only | Toggle | false | | Aims only at end crystals and ignores enemies. |
| Crystals → OnlyWhileUsing | Toggle | false | | Only aims at end crystals while you hold the use key (right click). |
| Requires | Multi-Select | | Click, MouseMovement, Weapon, EmptyHand, VanillaName, NotBreaking | Only aims when all picked conditions are true. Click: you are holding attack. MouseMovement: you moved your mouse in the last moment. Weapon: you hold a weapon. EmptyHand: your hand is empty. VanillaName: your item has no custom name. NotBreaking: you are not mining a block. |
| AngleSmooth | Choice | Interpolation | Interpolation, Sigmoid, Linear | How your view turns toward the enemy. Slower, smoother turns look more like a real player. |
| AngleSmooth → [Interpolation] → HorizontalSpeed | Integer Range | 80..85 | 1..100 % | How fast you turn left and right. |
| AngleSmooth → [Interpolation] → VerticalSpeed | Integer Range | 20..25 | 1..100 % | How fast you turn up and down. |
| AngleSmooth → [Interpolation] → DirectionChangeFactor | Integer Range | 95..100 | 0..100 % | How fast you turn when the enemy changes direction. |
| AngleSmooth → [Interpolation] → Midpoint | Decimal | 0.35 | 0.0..1.0 | Where during the turn you move fastest. |
| AngleSmooth → [Sigmoid] → HorizontalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | Fastest turn left and right, in degrees. |
| AngleSmooth → [Sigmoid] → VerticalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | Fastest turn up and down, in degrees. |
| AngleSmooth → [Sigmoid] → Steepness | Decimal | 10.0 | 0.0..20.0 | How quickly the turn speeds up and slows down. |
| AngleSmooth → [Sigmoid] → Midpoint | Decimal | 0.3 | 0.0..1.0 | Where during the turn you move fastest. |
| AngleSmooth → [Linear] → HorizontalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | How far you turn left and right at most, in degrees. |
| AngleSmooth → [Linear] → VerticalTurnSpeed | Decimal Range | 180.0..180.0 | 0.0..180.0 | How far you turn up and down at most, in degrees. |
| Axis | Multi-Select | Horizontal, Vertical | Horizontal, Vertical | Which way Aimbot may move your view: left and right (Horizontal), up and down (Vertical), or both. |
| Ignore | Multi-Select | | Screen, Container | Keeps aiming while a screen (Screen) or a chest or your inventory (Container) is open. |

---
*Last updated: 2026-11-14, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAimbot.kt)*
