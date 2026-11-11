## SpearKill

SpearKill lets you hit enemies with a charged spear from far away. While you charge a spear and hold attack, it dashes you to the enemy under your crosshair and right back to where you started. Enemies that are already close enough are skipped, and walls in the way stop the dash.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MaxTargetDistance | Decimal | 50.0 | 3.0..200.0 | How far away an enemy can be, in blocks. |
| MaxSpeed | Decimal | 7.0 | 2.0..10.0 | How fast the dash goes, in blocks per tick (20 ticks per second). |
| Preview | Toggleable Group | On | | Draws a box around the enemy you will hit while you charge. |
| Preview → FillColor | Color | Red | | Color inside the box. |
| Preview → OutlineColor | Color | White | | Color of the box's edges. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/spearkill/ModuleSpearKill.kt)*
