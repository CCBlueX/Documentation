## AutoTool

AutoTool silently swaps to the most efficient tool for whatever block you're breaking. The moment you start mining, it inspects the block, picks the best matching tool, and switches your held slot without you touching the hotbar — then swaps back to your previous slot after a short delay. It's the standard quality-of-life helper for mining, bridging, and bed-breaking so you never chip away at obsidian with your fist or waste durability on the wrong pick.

The **Dynamic** selector finds the best tool automatically; with **ConsiderInventory** on it will even pull a better tool out of your main inventory into the hotbar before mining. The **Static** selector instead always switches to one fixed hotbar slot. You can narrow what AutoTool reacts to with the **Filter**/**Blocks** list, and the [SilkTouchHandler test](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleAutoTool.kt#L157-L161) forces a Silk Touch tool for blocks that only drop themselves when mined with it (Ender Chest, Glowstone, Sea Lantern, Turtle Egg by default).

Several guards control *when* it acts: it can be limited to while sneaking, paused during combat, or restricted to when you're near a bed — all checked before [the swap is performed](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleAutoTool.kt#L211-L227).

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ToolSelector | Mode Selector | Dynamic | Dynamic, Static | How the tool is chosen: Dynamic finds the best tool automatically, Static always uses one fixed hotbar slot. |
| ToolSelector → [Dynamic] → IgnoreDurability | Toggle | false | — | When on, near-broken tools are still treated as eligible instead of being skipped to preserve durability. |
| ToolSelector → [Dynamic] → ConsiderInventory | Toggleable Group | Off | — | When on, also searches your main inventory for a better tool and swaps it into the hotbar before mining. |
| ToolSelector → [Dynamic] → ConsiderInventory → Constraints → StartDelay | Integer Range | 1..2 (ticks) | 0..20 | Ticks to wait before beginning the inventory swap. |
| ToolSelector → [Dynamic] → ConsiderInventory → Constraints → ClickDelay | Integer Range | 2..4 (ticks) | 0..20 | Ticks between inventory clicks while moving the tool. |
| ToolSelector → [Dynamic] → ConsiderInventory → Constraints → CloseDelay | Integer Range | 1..2 (ticks) | 0..20 | Ticks to wait before closing the inventory after the swap. |
| ToolSelector → [Dynamic] → ConsiderInventory → Constraints → MissChance | Integer Range | 0..0 (%) | 0..100 | Chance to intentionally misclick during the inventory swap, mimicking human imperfection. |
| ToolSelector → [Dynamic] → ConsiderInventory → Constraints → Requires | Multi-Select | [] | NoMovement, NoRotation, NotUsingItem, NotBreaking, NotDuringCombat | Conditions that must all be met before an inventory swap is allowed. |
| ToolSelector → [Static] → Slot | Integer | 0 | 0..8 | The fixed hotbar slot to switch to when breaking an eligible block. |
| Filter | Choice | Blacklist | Whitelist, Blacklist | Whether the Blocks list is a Whitelist (only act on listed blocks) or a Blacklist (act on everything except listed blocks). |
| Blocks | Registry List | — | — | The blocks the Filter applies to. |
| SilkTouchHandler | Toggleable Group | Off | — | When on, forces a Silk Touch tool for the configured blocks so they drop themselves. |
| SilkTouchHandler → Filter | Choice | Whitelist | Whitelist, Blacklist | Whether the SilkTouchHandler Blocks list is a Whitelist (only these blocks require Silk Touch) or a Blacklist. |
| SilkTouchHandler → Blocks | Registry List | — | — | Blocks that require a Silk Touch tool (defaults: Ender Chest, Glowstone, Sea Lantern, Turtle Egg). |
| SwapPreviousDelay | Integer | 20 (ticks) | 1..100 | Ticks to keep the selected tool before silently swapping back to your previous slot. |
| RequireSneaking | Toggle | false | — | Only switch tools while you are sneaking. |
| NotDuringCombat | Toggle | false | — | Don't switch tools while you are in combat. |
| RequireNearBed | Toggleable Group | Off | — | Only switch tools when a bed is within the configured distance. |
| RequireNearBed → Distance | Decimal | 10.0 | 3.0..50.0 | Maximum distance (in blocks) to a bed for the module to act. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleAutoTool.kt)*
