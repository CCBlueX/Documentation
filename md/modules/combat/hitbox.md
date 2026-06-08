## Hitbox

Hitbox makes the targets you're fighting easier to hit by expanding the invisible box the game uses to register your attacks. With a larger box, your crosshair doesn't have to be perfectly centered on an enemy for a swing to land, which helps when opponents are strafing, jittering, or fighting at the edge of your reach.

This pairs naturally with combat modules like [KillAura](/docs/modules/combat/killaura), [Aimbot](/docs/modules/combat/aimbot), and [Reach](/docs/modules/player/reach), giving you more forgiving aim during fast fights. Keep in mind that bigger hitboxes are very obvious to anti-cheats, so higher values are best reserved for casual or unprotected servers.

The **Size** value controls how much the box grows, while the two toggles decide which parts of the game's hit detection the enlargement is applied to.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Size | Decimal | 0.4 | 0.0..1.0 | How far the target's hitbox is expanded on each side. Higher values make enemies easier to hit but more obvious to anti-cheats. |
| ApplyToDebugHitbox | Toggle | true | — | Also enlarges the outline shown for entity hitboxes (visible with the F3+B debug view), so the displayed box matches the enlarged hit area. |
| ApplyToComponent | Toggle | true | — | Applies the enlargement to items that define their own attack range, keeping the expanded hitbox consistent when using such weapons. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleHitbox.kt)*
