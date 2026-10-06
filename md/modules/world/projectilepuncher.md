## ProjectilePuncher

ProjectilePuncher automatically deflects dangerous incoming projectiles — specifically ghast fireballs and shulker bullets — by punching them back before they can hit you. When one of these projectiles is detected within range and heading in your direction, the module aims at it and attacks, sending it back the way it came.

The module only targets projectiles that are actually on a collision course with you, so it won't waste clicks on fireballs flying past harmlessly. Aim corrections are handled smoothly through the [Shared: Rotations](/docs/modules/shared-settings/rotations) system, and click timing is controlled by the [Shared: Clicker](/docs/modules/shared-settings/clicker) group, letting you tune the attack rate to suit your needs or bypass anti-cheat checks.

This module pairs well with [CrystalAura](/docs/modules/combat/crystalaura) and other combat modules when fighting in the Nether or End where ghasts and shulkers are common threats.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Clicker | Setting Group | — | — | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Range | Decimal | 3.0 | 3.0..6.0 | Maximum distance (in blocks) at which incoming projectiles will be targeted and punched. |
| SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Controls how the arm swing animation is shown when attacking a projectile. |
| IgnoreOpenInventory | Toggle | true | — | When enabled, the module will still aim and attack projectiles even if you have an inventory screen open. |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleProjectilePuncher.kt)*
