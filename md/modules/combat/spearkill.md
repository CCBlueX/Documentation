## SpearKill

SpearKill automatically attacks enemies using a charged spear. While you charge a spear (held in either hand) and hold the attack key, the module picks the target your crosshair is pointing at and dashes you toward its predicted position, then immediately reverses the movement so you end up back where you started. This lets you land the spear's charge attack on enemies far beyond its normal reach.

A target is only selected if it is between 3 blocks and **MaxTargetDistance** away, you have line of sight to it, and the dash path is not blocked by terrain. **MaxSpeed** caps how fast the dash travels; higher values reach the target in fewer ticks. The dash starts only while the spear's charge is still building up — once the charge completes or you release the attack key, nothing happens.

With the **Preview** group enabled, the current target is highlighted with a colored box while you charge, so you can see who the dash will hit before committing. For the Ender Dragon, all of its body parts are highlighted.

**Category:** Combat
**Aliases:** AutoSpear
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MaxTargetDistance | Decimal | 50.0 | 3.0 – 200.0 | Maximum distance at which enemies can be targeted. Targets closer than 3 blocks are ignored. |
| MaxSpeed | Decimal | 7.0 | 2.0 – 10.0 | Maximum dash speed in blocks per tick. |
| Preview | Toggleable Group | On | — | Highlights the currently selected target with a box while you charge the spear. |
| Preview → FillColor | Color | Red (alpha 67) | — | Fill color of the target highlight box. |
| Preview → OutlineColor | Color | White (alpha 167) | — | Color of the highlight box's outline. |

---
*Last updated: 2026-07-16 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/master/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleSpearKill.kt)*
