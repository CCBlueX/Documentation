## ItemScroller

ItemScroller lets you quickly move items through your inventory by holding **Shift** and **left-clicking** while scrolling over inventory slots. Instead of individually shift-clicking each slot, you can sweep your cursor across multiple items in one smooth motion to transfer them all rapidly.

This is especially handy when looting chests, sorting your inventory, or quickly moving stacks between containers. The **Delay** setting introduces a small randomised pause between each click action, which helps the behaviour look more natural on servers with anti-cheat detection.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ClickMode | Choice | QuickMove | — | Determines how items are moved when scrolling. `QuickMove` performs a shift-click (quick move) on each slot you hover over. |
| Delay | Integer Range | 2..3 | 0..20 ticks | A randomised delay between successive scroll-triggered click actions. Higher values add more time between clicks; set to `0..0` for no delay. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleItemScroller.kt)*
