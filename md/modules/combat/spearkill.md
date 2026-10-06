## SpearKill

SpearKill automatically attacks enemies using a charged spear. While you charge a spear (held in either hand) and hold the attack key, the module picks the target your crosshair is pointing at and dashes you toward its predicted position, then immediately reverses the movement so you end up back where you started. This lets you land the spear's charge attack on enemies far beyond its normal reach.

A target is only selected if it is within **MaxTargetDistance**, you have line of sight to it, and the dash path is not blocked by terrain. Enemies that already sit inside the spear's damage window are skipped, since no dash is needed to reach them. The dash covers only the distance needed to bring the target into that window rather than carrying you all the way onto it. **MaxSpeed** caps how fast the dash travels; higher values reach the target in fewer ticks. The dash starts once the spear's charge delay has passed and only while the charge attack can still deal damage — releasing the attack key stops it.

While you keep the use key held, the module releases and re-uses the spear for you once its charge attack has been spent, so the next charge begins without letting go of the key. A dash that is still in flight is never interrupted by this, so its return movement always brings you back to where you started.

With the **Preview** group enabled, the current target is highlighted with a colored box while you charge, so you can see who the dash will hit before committing. For the Ender Dragon, all of its body parts are highlighted.

**Category:** Combat
**Aliases:** AutoSpear
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MaxTargetDistance | Decimal | 50.0 | 3.0 – 200.0 | Maximum distance at which enemies can be targeted. Targets already within the spear's damage window are ignored. |
| MaxSpeed | Decimal | 7.0 | 2.0 – 10.0 | Maximum dash speed in blocks per tick. |
| Preview | Toggleable Group | On | — | Highlights the currently selected target with a box while you charge the spear. |
| Preview → FillColor | Color | Red (alpha 67) | — | Fill color of the target highlight box. |
| Preview → OutlineColor | Color | White (alpha 167) | — | Color of the highlight box's outline. |

---
*Last updated: 2026-09-26 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/master/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/spearkill/ModuleSpearKill.kt)*
