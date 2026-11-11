## AutoClicker

AutoClicker clicks for you while you hold a mouse button, so you don't have to click fast yourself. The Attack part clicks the left button, the Use part clicks the right button. It does not aim for you. To attack enemies under your crosshair without holding the button, use [TriggerBot](/docs/modules/combat/triggerbot).

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Attack | Toggleable Group | On | | Clicks the attack button (left click) while you hold it. |
| Attack → Clicker | Setting Group | | | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Attack → DelayOnBroken | Toggle | true | | Waits a moment after you break a block before clicking again. |
| Attack → Objective | Choice | Any | Enemy, Entity, Block, Any | What your crosshair has to be on for it to click: an enemy, any entity, a block, or anything. |
| Attack → OnItemUse | Choice | Wait | Wait, Stop, Ignore | What to do while you use an item, like eating. Wait waits until you are done. Stop stops using the item. Ignore keeps clicking anyway. |
| Attack → Weapon | Multi-Select | Any | Any, Sword, Axe, Mace, Spear, Pickaxe, Shovel, Hoe, Knockback, FireAspect | Only clicks while you hold one of these. Knockback and FireAspect mean any item with that enchantment. |
| Attack → Criticals | Choice | Smart | Smart, Ignore, Always | When to wait for a critical hit. Smart waits when a critical hit is possible soon. Ignore never waits. Always only hits when it is a critical hit. |
| Attack → DelayPostStopUse | Integer | 0 | 0..20 ticks | How long to wait after you stop using an item before clicking again, in ticks (20 per second). |
| Use | Toggleable Group | Off | | Clicks the use button (right click) while you hold it. |
| Use → Clicker | Setting Group | | | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Use → HoldingItemsForIgnore | Registry List | Water Bucket, Lava Bucket, Ender Pearl, Eye of Ender, Player Head | | Does not click while you hold one of these items. |
| Use → BlocksForIgnore | Registry List | Doors, fence gates, trapdoors | | Does not click while you look at one of these blocks. |
| Use → DelayStart | Toggle | false | | Waits a moment before the first click. |
| Use → OnlyBlock | Toggle | false | | Only clicks while you hold a block. |
| Use → RequiresNoInput | Toggle | false | | Clicks even when you are not holding right click. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/autoclicker/ModuleAutoClicker.kt)*
