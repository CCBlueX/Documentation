## AutoShoot

AutoShoot throws eggs and snowballs at the closest enemy you can see. It is made for minigames where you shoot things at each other, like QuakeCraft, Lasertag or Paintball. You can also pick your own list of items to throw.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ThrowableType | Choice | EggAndSnowball | EggAndSnowball, Custom | What to throw. EggAndSnowball uses eggs and snowballs. Custom uses the items you pick. |
| ThrowableType → [Custom] → Filter | Choice | Whitelist | Whitelist, Blacklist | Whitelist throws only the listed items. Blacklist throws anything except the listed items. |
| ThrowableType → [Custom] → Items | Registry List | Egg, Snowball | | The items for the filter. |
| GravityType | Choice | Auto | Auto, Linear, Projectile | How to aim. Linear looks straight at the enemy. Projectile aims higher so the thrown item's curve lands on them. Auto uses Projectile for eggs and snowballs and Linear for anything else. |
| Clicker | Setting Group |  | | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Range | Decimal Range | 3.0..6.0 | 1.0..256.0 | How far away an enemy can be, in blocks. |
| Target | Setting Group |  | | See [Shared: Target](/docs/modules/shared-settings/target). |
| AimPoint | Setting Group |  | | See [Shared: AimPoint](/docs/modules/shared-settings/aimpoint). |
| Rotations | Setting Group |  | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| AimOffThreshold | Decimal | 2.0 | 0.5..10.0 | How far off your aim can be, in degrees, and still throw. |
| SwingMode | Choice | DoNotHide | DoNotHide, HideForClient | Whether you see your arm swing when you throw. |
| TargetRendering | Toggleable Group | On | | See [Shared: TargetRendering](/docs/modules/shared-settings/targetrendering). |
| SelectSlotAutomatically | Toggle | true | | Switches to the item to throw by itself. When off, it only throws while you already hold one. |
| TicksUntilSlotReset | Integer | 1 | 0..20 | How many ticks (20 per second) to wait before switching back to your old item. |
| ConsiderInventory | Toggle | true | | Does not aim or throw while your inventory is open. |
| RequiresKillAura | Toggle | false | | Only works while [KillAura](/docs/modules/combat/killaura) is on. |
| NotDuringCombat | Toggle | false | | Does not throw while you are fighting. |
| ConstantLag | Toggle | false | | While [FakeLag](/docs/modules/combat/fakelag) is also on, it lags all the time when AutoShoot has no target. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoShoot.kt)*
