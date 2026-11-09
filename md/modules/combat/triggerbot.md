## TriggerBot

TriggerBot attacks the enemy under your crosshair without you holding the attack button. It only clicks when your crosshair is on an entity that should be attacked, so it never swings at air, blocks or entities that aren't targets. Click timing is controlled through the shared [Clicker](/docs/modules/shared-settings/clicker) group.

It shares its attack settings with the Attack part of [AutoClicker](/docs/modules/combat/autoclicker), which only clicks while you hold the attack button. Like AutoClicker, TriggerBot does not aim for you — it only attacks where you're already looking. Pair it with [Aimbot](/docs/modules/combat/aimbot) if you want your view to follow targets.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Clicker | Setting Group | — | — | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| OnItemUse | Choice | Wait | Wait, Stop, Ignore | How to react while you're using an item — wait for it to finish, stop using it, or ignore it. |
| Weapon | Multi-Select | [Any] | Any, Sword, Axe, Mace, Spear, Pickaxe, Shovel, Hoe, Knockback, FireAspect | Only attacks when one of these weapon types is in your main hand. |
| Criticals | Choice | Smart | Smart, Ignore, Always | When to time clicks for critical hits. |
| DelayPostStopUse | Integer | 0 | 0–20 ticks | Extra wait after an item use ends before resuming attacks. |

---
*Last updated: 2026-11-09 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/autoclicker/ModuleTriggerBot.kt)*
