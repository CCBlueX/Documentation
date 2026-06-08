## ElytraSwap

ElytraSwap lets you instantly switch between your chestplate and an elytra with a single action. When you trigger it, the module looks at your hotbar, main inventory, and offhand for the appropriate item and swaps it onto your chest slot for you — no need to open your inventory and drag items around. If your chest slot is empty it equips an elytra; if you're wearing an elytra it puts your chestplate back on; and if you're wearing a chestplate it switches to your elytra.

This is handy for situations where you constantly alternate between fighting in full armor and flying with an elytra, letting you change gear in a fraction of a second. The module only picks an elytra that isn't about to break, so it won't equip a worn-out wing.

ElytraSwap performs its swap once and then disables itself automatically, so you simply re-enable it (for example with a bind) each time you want to switch. It also turns itself off when you leave a server.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleElytraSwap.kt)*
