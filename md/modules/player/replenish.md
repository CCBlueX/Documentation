## Replenish

Replenish automatically tops up your hotbar slots from your main inventory whenever a stack runs low. Once a slot drops to or below the **ItemThreshold**, the module finds matching items in your inventory and moves them over — no manual restocking needed. This is particularly useful when consuming large quantities of a single item type, such as building blocks with [Scaffold](/docs/modules/world/scaffold), food, arrows, or potions.

By default, Replenish only activates while you are playing in the world normally. You can optionally allow it to run while your inventory screen is open, or even while you have a chest (or other container) open, using the **InsideOf** setting. The **Features** multi-select lets you fine-tune how refills are performed: **CleanUp** merges smaller partial stacks first to tidy your inventory, **UsePickupAll** picks up all matching stacks directly onto the hotbar slot, and **UseSwap** does a direct slot swap when a bigger inventory stack is available — choose the combination that best fits your play style and the anti-cheat environment you are on.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| ItemThreshold | Integer | 5 | 0 – 63 | When a hotbar stack's count falls to this value or below, the module will attempt to refill it from your inventory. |
| Delay | Integer | 40 | 0 – 1000 ms | Minimum time in milliseconds between consecutive refill actions. |
| ReplenishEmpty | Toggle | true | — | When enabled, also refills hotbar slots that are completely empty (using the last known item for that slot). |
| Features | Multi-Select | CleanUp | CleanUp, UsePickupAll, UseSwap | Controls how refills are performed. **CleanUp** consolidates smaller partial stacks first; **UsePickupAll** merges all matching stacks onto the hotbar slot; **UseSwap** swaps a larger inventory stack directly into the hotbar slot. |
| InsideOf | Multi-Select | *(none)* | Chests, Inventories | Allows Replenish to operate while specific screens are open. Add **Chests** to run inside container screens, or **Inventories** to run while your own inventory screen is open. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleReplenish.kt)*
