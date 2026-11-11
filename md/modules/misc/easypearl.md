## EasyPearl

EasyPearl throws ender pearls to the block you look at. Look at a spot, press use, and it turns you to the right angle and throws. While you hold a pearl, a box shows the spot: green means the pearl can reach it, red means it can't.

It works with pearls in your hotbar or offhand. For pearls thrown for you during fights, see [AutoPearl](/docs/modules/combat/autopearl).

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| AimOffThreshold | Decimal | 2.0 | 0.5..10.0 | How close (in degrees) your aim has to be to the right angle before it throws. Lower is more exact. |
| ReachableCheck | Toggle | true | | Doesn't throw at spots the pearl can't reach and warns you instead. |
| Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| ShowDistance | Toggle | true | | Shows how far away the spot is. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleEasyPearl.kt)*
