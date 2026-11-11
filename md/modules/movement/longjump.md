## LongJump

LongJump makes your jumps go much farther forward. Use it to get across big gaps. Pick the mode that matches the anti-cheat on your server.

NCP-3.16.1-Bow needs a bow and arrows. It shoots arrows straight up to hit yourself, then jumps forward with the knockback.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | NCP-3.16.1-Boost | NCP-3.16.1-Boost, NCP-3.16.1-Bow, Vulcan-2.8.9, Matrix-7.14.5-Flag | How the long jump works. |
| Mode → [NCP-3.16.1-Boost] → NCPBoost | Decimal | 4.25 | 1.0..10.0 | How much faster you go when you jump. Higher goes farther but gets caught more easily. |
| Mode → [NCP-3.16.1-Bow] → Rotations | Setting Group |  |  | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [NCP-3.16.1-Bow] → Charged | Integer | 4 | 3..20 | How long to pull the bow before each shot, in ticks (20 per second). |
| Mode → [NCP-3.16.1-Bow] → Speed | Decimal | 2.5 | 0.0..20.0 | How fast you fly forward after the arrows hit. |
| Mode → [NCP-3.16.1-Bow] → ArrowsToShoot | Integer | 8 | 0..20 | How many arrows to shoot before the jump. |
| Mode → [NCP-3.16.1-Bow] → FallDistanceToJump | Decimal | 0.42 | 0.0..2.0 | How far you need to fall before the next jump. |
| Mode → [Matrix-7.14.5-Flag] → BoostSpeed | Decimal | 1.97 | 0.1..5.0 | How fast each boost pushes you forward. |
| Mode → [Matrix-7.14.5-Flag] → MotionY | Decimal | 0.42 | 0.0..5.0 | How high each boost pushes you. |
| Mode → [Matrix-7.14.5-Flag] → Delay | Integer | 0 | 0..3 | Ticks to wait after leaving the ground before the boost. |
| AutoJump | Toggle | false |  | Jump by itself while you walk. |
| DisableAfterFinished | Toggle | false |  | Turn LongJump off after one long jump. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/longjump/ModuleLongJump.kt)*
