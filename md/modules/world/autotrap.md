## AutoTrap

AutoTrap places cobwebs on nearby enemies, or sets them on fire with lava or flint and steel. Webs slow an enemy down so they can't run. Fire hurts them over time.

You need cobwebs, a lava bucket or flint and steel in your hotbar or offhand. If an enemy jumps or falls, AutoTrap places the trap where they will land. It tries a web first and uses fire if that doesn't work. While you fight with KillAura, it waits for a good moment so it doesn't ruin your hits.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal Range | 3.0..4.5 | 2.0..6.0 blocks | How far away an enemy can be. |
| Delay | Integer | 20 | 0..400 ticks | How long to wait after a trap before the next one, in ticks (20 per second). |
| IgnoreOpenInventory | Toggle | true | | Keeps working while a chest or your inventory is open. |
| Ignite | Toggleable Group | On | | Sets enemies on fire with lava or flint and steel. Skips enemies that are already burning. |
| AutoWeb | Toggleable Group | On | | Places cobwebs on enemies. |
| Target | Setting Group | | | See [Target](/docs/modules/shared-settings/target). |
| Rotations | Setting Group | | | See [Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/traps/ModuleAutoTrap.kt)*
