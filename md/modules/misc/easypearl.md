## EasyPearl

EasyPearl makes throwing ender pearls far more reliable. Instead of guessing the arc, just look at the spot you want to land on, hold down your use key, and the module works out the throwing angle for you — accounting for the pearl's trajectory — before releasing it toward that point.

When you trigger a throw, EasyPearl first turns your aim to the calculated angle and only lets the pearl fly once you're pointing the right way, so your toss lands where you intended. While you're holding a pearl, a colored box highlights the block you're aiming at: green means the spot is reachable and the throw will work, red means it's out of range. With ReachableCheck on, throws at unreachable spots are blocked and you get a warning instead of wasting the pearl.

It works with pearls in either your main hand or offhand. For automatic combat pearling instead of manual aiming, see [AutoPearl](/docs/modules/combat/autopearl).

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| AimOffThreshold | Decimal | 2.0 | 0.5..10.0 | How close your aim must be to the calculated throwing angle (in degrees) before the pearl is released. Lower values demand a more precise alignment for greater accuracy; higher values let the pearl fly sooner. |
| ReachableCheck | Toggle | true | — | When on, blocks throws at spots the pearl can't actually reach and shows a warning instead, preventing wasted pearls. |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleEasyPearl.kt)*
