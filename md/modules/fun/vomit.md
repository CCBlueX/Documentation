## Vomit

Vomit continuously throws items out of your inventory in a random order, creating the visual effect of your character vomiting its entire inventory onto the ground. Each tick, a random occupied slot is picked and its stack is dropped — making it a chaotic and entertaining way to clear your inventory or just mess around on a server.

In **survival mode**, the module picks random non-empty slots from your inventory (or from an open container if your inventory is already empty) and drops them one by one. In **creative mode**, it instead spawns random block stacks out of thin air and immediately throws them, so the "vomiting" never stops regardless of what you're carrying.

The speed and timing of drops are governed by the Inventory Constraints settings below, so you can tune how fast items fly out.

**Category:** Fun
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/fun/ModuleVomit.kt)*
