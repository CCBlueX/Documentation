## ProjectilePuncher

ProjectilePuncher hits ghast fireballs, shulker bullets and wind charges that fly toward you, so they get knocked away before they hit you. It only goes for ones that would actually hit you.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Clicker | Setting Group | | | See [Clicker](/docs/modules/shared-settings/clicker). |
| Range | Decimal | 3.0 | 3.0..6.0 | How close a fireball or bullet must be. |
| SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Whether your arm swing is shown. |
| IgnoreOpenInventory | Toggle | true | | Keeps working while your inventory is open. |
| Projectiles | Multi-Select | Fireball, ShulkerBullet | Fireball, ShulkerBullet, WindCharge | Which flying things it hits. |
| OnlyInAir | Toggle | false | | Only hits them while you are in the air. |
| FOV | Decimal | 180.0 | 0.0..180.0 ° | How far from where you are looking a target can be. |
| Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-11-15, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/master/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleProjectilePuncher.kt)*
