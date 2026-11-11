## Target

The Target settings decide which players and mobs a module goes after, and which one it picks first. Who counts as an enemy at all (players, mobs, friends, teams) is set in the global [Targets](/docs/global-settings/targets) settings.

Used by: [KillAura](/docs/modules/combat/killaura), [Aimbot](/docs/modules/combat/aimbot), [AutoBow](/docs/modules/combat/autobow), [AutoRod](/docs/modules/combat/autorod), [AutoShoot](/docs/modules/combat/autoshoot), [CrystalAura](/docs/modules/combat/crystalaura), [ElytraTarget](/docs/modules/combat/elytratarget), [ProjectileAimbot](/docs/modules/combat/projectileaimbot), [TpAura](/docs/modules/combat/tpaura), [TargetStrafe](/docs/modules/movement/targetstrafe), [BlockTrap](/docs/modules/world/blocktrap), [AutoTrap](/docs/modules/world/autotrap).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| FOV | Decimal | 180.0 | 0.0..180.0 | How far from where you are looking an enemy can be, in degrees. 180 means anywhere around you. Lower values only pick enemies near the middle of your screen. |
| HurtTime | Integer | 10 | 0..10 | Skips enemies that were hit very recently. 10 picks everyone. 0 only picks enemies that are not flashing red from a hit. |
| Priority | Multi-Select | Type and one more that depends on the module | Type, Health, Distance, Direction, HurtTime, Age | Which enemy to pick first. The first picked option counts most, the next one decides ties, and so on. At least one has to be picked. |

### Priority options

- Type: players first, then hostile mobs, then everything else.
- Health: the enemy with the least health first.
- Distance: the closest enemy first.
- Direction: the enemy closest to your crosshair first.
- HurtTime: the enemy that can take damage again soonest first.
- Age: the enemy that has been in the world longest first. Bots that just appeared come last.

Some modules add a **Range** setting to this group, which sets how far away an enemy can be.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/combat/TargetTracker.kt)*
