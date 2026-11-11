## TriggerBot

TriggerBot attacks when your crosshair is on an enemy, without you holding the attack button. It never swings at air or blocks. It does not aim for you, so you can use it with [Aimbot](/docs/modules/combat/aimbot) if you want your view to follow enemies.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Clicker | Setting Group | | | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| OnItemUse | Choice | Wait | Wait, Stop, Ignore | What to do while you use an item, like eating. Wait waits until you are done. Stop stops using the item. Ignore keeps clicking anyway. |
| Weapon | Multi-Select | Any | Any, Sword, Axe, Mace, Spear, Pickaxe, Shovel, Hoe, Knockback, FireAspect | Only attacks while you hold one of these. Knockback and FireAspect mean any item with that enchantment. |
| Criticals | Choice | Smart | Smart, Ignore, Always | When to wait for a critical hit. Smart waits when a critical hit is possible soon. Ignore never waits. Always only hits when it is a critical hit. |
| DelayPostStopUse | Integer | 0 | 0..20 ticks | How long to wait after you stop using an item before attacking again, in ticks (20 per second). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/autoclicker/ModuleTriggerBot.kt)*
