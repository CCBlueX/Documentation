## AutoShoot

AutoShoot automatically throws projectiles — eggs and snowballs by default — at the nearest enemy it can see. It was built mainly for Hypixel QuakeCraft, but works well in other projectile-based minigames such as Cytooxien Lasertag and Paintball, and replaces the older AutoBalls module with more accurate aiming. Each tick it picks the closest visible target within [your configured Range](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoShoot.kt#L82), works out the rotation needed to hit it, and fires once it's aimed close enough.

The clever part is the aiming. The module [pre-aims a tick ahead](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoShoot.kt#L153-L173) so it can react the instant you peek around a corner, and the **GravityType** option decides how it leads the shot. On *Auto* it [uses a full gravity-compensating trajectory](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoShoot.kt#L274-L284) for eggs and snowballs (which arc), and aims straight at the hitbox for fast, flat-flying projectiles. It only releases the throw once your server-side rotation is within **AimOffThreshold** degrees of the target, and only when you aren't already using an item.

You can keep AutoShoot to vanilla throwables or switch **ThrowableType** to *Custom* to define your own whitelist or blacklist of items to throw. It can grab and select the right hotbar slot for you automatically, and pause itself when your inventory is open, when you're in combat, or until KillAura is active — useful for combining it with melee combat without conflicts.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ThrowableType | Mode Selector | EggAndSnowball | EggAndSnowball, Custom | Chooses which items count as throwables. *EggAndSnowball* only uses vanilla eggs and snowballs; *Custom* lets you define your own item set. |
| ThrowableType → [Custom] → Filter | Choice | Whitelist | Whitelist, Blacklist | Whether the item list below is treated as items to allow (*Whitelist*) or items to exclude (*Blacklist*). |
| ThrowableType → [Custom] → Items | Registry List | — | — | The list of items the filter applies to (defaults to Egg and Snowball). |
| GravityType | Choice | Auto | Auto, Linear, Projectile | How the shot is led. *Auto* uses gravity-compensated trajectory for eggs/snowballs and straight aim for everything else; *Linear* aims directly at the hitbox; *Projectile* always computes a gravity-aware throwing angle. |
| Clicker | Setting Group | — | — | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Range | Decimal Range | 3.0..6.0 | 1.0..256.0 | Distance window (in blocks) within which a target is considered valid for shooting. |
| Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |
| AimPoint | Setting Group | — | — | See [Shared: AimPoint](/docs/modules/shared-settings/aim-point). |
| Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| AimOffThreshold | Decimal | 2.0 | 0.5..10.0 | Maximum allowed angle (in degrees) between your server-side rotation and the target before the throw is released; smaller values demand tighter aim. |
| SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Controls whether and where the arm-swing animation is shown when throwing. |
| TargetRendering | Toggleable Group (on) | on | — | See [Shared: TargetRendering](/docs/modules/shared-settings/target-rendering). |
| SelectSlotAutomatically | Toggle | true | — | When enabled, automatically switches to the hotbar slot holding a throwable so it can shoot; if off, it only shoots when you already hold one. |
| TicksUntilSlotReset | Integer | 1 | 0..20 | How many ticks to keep the silently-selected slot active before reverting to your previous slot. |
| ConsiderInventory | Toggle | true | — | When enabled, holds off on aiming and throwing while your inventory screen is open. |
| RequiresKillAura | Toggle | false | — | When enabled, only runs while KillAura is active, pausing otherwise. |
| NotDuringCombat | Toggle | false | — | When enabled, pauses shooting while you are in combat. |
| ConstantLag | Toggle | false | — | Internal compensation flag used by other systems when reasoning about AutoShoot's timing. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoShoot.kt)*
