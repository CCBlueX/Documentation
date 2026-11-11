## AutoTool

AutoTool picks the best tool in your hotbar when you start breaking a block. After you stop, it switches back to the item you held before.

It can also use a Silk Touch tool for blocks that only drop themselves with Silk Touch, like Ender Chests and Glowstone.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ToolSelector | Mode Selector | Dynamic | Dynamic, Static | Dynamic finds the best tool. Static always uses one hotbar slot. |
| ToolSelector → [Dynamic] → IgnoreDurability | Toggle | false | | Also uses tools that are almost broken. |
| ToolSelector → [Dynamic] → ConsiderInventory | Toggleable Group | Off | | Also looks in your inventory and moves a better tool into the hotbar. |
| ToolSelector → [Dynamic] → ConsiderInventory → Constraints | Setting Group | | | See [Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| ToolSelector → [Static] → Slot | Integer | 0 | 0..8 | The hotbar slot to switch to. |
| Filter | Choice | Blacklist | Whitelist, Blacklist | Whitelist: only work on the listed blocks. Blacklist: work on all blocks except the listed ones. |
| Blocks | Registry List | | | The blocks the filter uses. |
| SilkTouchHandler | Toggleable Group | Off | | Chooses Silk Touch on purpose for some blocks. |
| SilkTouchHandler → Filter | Choice | Whitelist | Whitelist, Blacklist | Whitelist: use a Silk Touch tool on the listed blocks. Blacklist: use a tool without Silk Touch on them. |
| SilkTouchHandler → Blocks | Registry List | Ender Chest, Glowstone, Sea Lantern, Turtle Egg | | The blocks this applies to. |
| SwapBackDelay | Integer | 20 | 1..100 ticks | How long to wait before switching back to your old item, in ticks (20 per second). |
| SwitchDelay | Integer | 0 | 0..100 ticks | How long you mine a block with your current item before the tool is picked. |
| RequireSneaking | Toggle | false | | Only switch while you sneak. |
| NotDuringCombat | Toggle | false | | Don't switch while you are fighting. |
| RequireNearBed | Toggleable Group | Off | | Only switch when a bed is close. |
| RequireNearBed → Distance | Decimal | 10.0 | 3.0..50.0 blocks | How close the bed has to be. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleAutoTool.kt)*
