## AutoClicker

AutoClicker automatically fires clicks for you while you hold down a mouse button, so you don't have to spam your mouse. It's split into two independent parts: one for the **attack** (left) button and one for the **use** (right) button. Each part has its own click-speed timing, controlled through its shared [Clicker](/docs/modules/shared-settings/clicker) group.

The Attack part keeps you swinging at whatever your crosshair is pointed at, which is why it's also known as a triggerbot. You can restrict it to only attack enemies, any entity, blocks, or anything at all, and limit it to specific weapon types so it won't swing with the wrong item. It can also respect critical hits and pause itself while you're eating or using an item. Unlike [KillAura](/docs/modules/combat/killaura), it does not aim for you — it only clicks where you're already looking.

The Use part auto-clicks the right button, which is handy for rapidly placing blocks or interacting. It can be limited to only block items and will skip clicking when you're holding certain items (like buckets, pearls, or eyes) or looking at blocks you'd rather open manually, such as doors, gates, and trapdoors.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Attack | Toggleable Group | Off | — | Auto-clicks the attack (left) button while it's held. |
| Attack → Clicker | Setting Group | — | — | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Attack → RequiresNoInput | Toggle | false | — | Clicks even when you aren't physically holding the attack button. |
| Attack → DelayOnBroken | Toggle | true | — | Briefly pauses clicking right after you finish breaking a block. |
| Attack → Objective | Choice | Enemy | Enemy, Entity, Block, Any | What your crosshair must be on for it to click. |
| Attack → OnItemUse | Choice | Wait | Wait, Stop, Ignore | How to react while you're using an item — wait for it to finish, stop using it, or ignore it. |
| Attack → Weapon | Multi-Select | [Any] | Any, Sword, Axe, Mace, Spear, Pickaxe, Shovel, Hoe, Knockback, FireAspect | Only clicks when one of these weapon types is in your main hand. |
| Attack → Criticals | Choice | Smart | Smart, Ignore, Always | When to time clicks for critical hits. |
| Attack → DelayPostStopUse | Integer | 0 | 0–20 ticks | Extra wait after an item use ends before resuming clicks. |
| Use | Toggleable Group | On | — | Auto-clicks the use (right) button while it's held. |
| Use → Clicker | Setting Group | — | — | See [Shared: Clicker](/docs/modules/shared-settings/clicker). |
| Use → HoldingItemsForIgnore | Registry List | — | — | Items that, when held in either hand, stop it from clicking. |
| Use → BlocksForIgnore | Registry List | — | — | Blocks that, when looked at, stop it from clicking. |
| Use → DelayStart | Toggle | false | — | Adds a short delay before the first click after you start holding. |
| Use → OnlyBlock | Toggle | true | — | Only clicks when you're holding a placeable block. |
| Use → RequiresNoInput | Toggle | false | — | Clicks even when you aren't physically holding the use button. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/ModuleAutoClicker.kt)*
