## AutoRod

AutoRod throws a fishing rod at enemies close to you and pulls it back in. The hook knocks them back a bit and can break their combo. You need a fishing rod in your hotbar or offhand.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| GravityType | Choice | Linear | Linear, Projectile | How to aim. Linear looks straight at the enemy. Projectile aims higher so the hook's curve lands on them. |
| Range | Decimal Range | 3.5..5.0 | 2.0..10.0 | How close an enemy has to be, in blocks. |
| ScanExtraRange | Decimal Range | 0.0..0.0 | 0.0..5.0 | A random extra distance added to the far end of Range for each throw. |
| MaxEnemiesNearby | Integer | 1 | 0..10 | Only throws when there are at most this many enemies around. 0 means any number. |
| MinHealth | Decimal | 10.0 | 1.0..20.0 | Only throws while your health is above this. |
| MinTargetHealth | Decimal | 4.0 | 1.0..20.0 | Only throws at enemies whose health is above this. |
| Requires | Multi-Select | Click, Weapon, VanillaName, NotBreaking | Click, Weapon, EmptyHand, VanillaName, NotBreaking | Only throws when all picked conditions are true. Click: you are holding attack. Weapon: you hold a weapon. EmptyHand: your hand is empty. VanillaName: your item has no custom name. NotBreaking: you are not mining a block. |
| Ignore | Multi-Select | | OpenInventory, UsingItem, HoldingConsumable | Does not throw while any picked thing is true: your inventory is open, you are using an item, or you hold food or a potion. |
| HoldingItemsForIgnore | Registry List | Bow, Crossbow, Trident, Fire Charge, Ender Pearl | | Does not throw while you hold one of these items. |
| Target | Setting Group |  | | See [Shared: Target](/docs/modules/shared-settings/target). |
| AimPoint | Setting Group |  | | See [Shared: AimPoint](/docs/modules/shared-settings/aimpoint). |
| Rotations | Setting Group |  | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| AimOffThreshold | Decimal | 5.0 | 2.0..10.0 | How far off your aim can be, in degrees, and still throw. |
| SwingMode | Choice | DoNotHide | DoNotHide, HideForClient | Whether you see your arm swing when you use the rod. |
| TargetRendering | Toggleable Group | On | | See [Shared: TargetRendering](/docs/modules/shared-settings/targetrendering). |
| HitTimeout | Integer | 30 | 5..200 ticks | How long to wait for the hook to hit before pulling it back, in ticks (20 per second). |
| PullOnOutOfRange | Toggle | true | | Pulls the hook back right away when the enemy leaves your range. |
| SlotResetDelay | Integer Range | 0..0 | 0..20 ticks | How long to wait after pulling in before switching back to your old item. |
| Cooldown | Integer Range | 4..8 | 1..50 ticks | How long to wait before the next throw. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoRod.kt)*
