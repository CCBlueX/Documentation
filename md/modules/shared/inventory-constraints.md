## Inventory Constraints

The Inventory Constraints setting group controls the timing, requirements, and humanization of automated inventory actions. It enforces delays between opening, clicking, and closing inventory screens, and can require certain conditions (such as the player standing still) to be met before any action is performed.

The Inventory Constraints setting group appears in the following modules:
- [AutoArmor](/docs/modules/combat/autoarmor)
- [ChestStealer](/docs/modules/player/cheststealer)
- [ChestCleaner](/docs/modules/player/chestcleaner)
- [InventoryCleaner](/docs/modules/player/inventorycleaner)
- [Replenish](/docs/modules/player/replenish)
- [Offhand](/docs/modules/player/offhand)
- [AutoTool](/docs/modules/world/autotool)

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| StartDelay | Integer Range | 1..2 | 0..20 ticks | The number of ticks to wait after the inventory is first opened (or after a screen is detected) before performing the first click action. A random value within this range is chosen each time. |
| ClickDelay | Integer Range | 2..4 | 0..20 ticks | The number of ticks to wait between each successive click action. Also applied after a simulated miss click. A random value within this range is chosen each time. |
| CloseDelay | Integer Range | 1..2 | 0..20 ticks | The number of ticks to wait before closing the inventory after all scheduled actions are completed. A random value within this range is chosen each time. |
| MissChance | Integer Range | 0..0 | 0..100 % | The percentage chance that the first click in an action chain is replaced with a simulated miss click (clicking on an empty or wrong slot). Only applies to container-type click actions and does not apply to throw actions. When a miss click occurs, the normal click delay is waited before retrying the intended action. |
| Requires | Multi-Select | [] | NoMovement, NoRotation, InventoryOpen\* | A set of conditions that must all be met before any inventory action is allowed to proceed. If any selected requirement is not satisfied, the action is postponed. See [Requirements](#requirements) for details. |

\*InventoryOpen is only available in `PlayerInventoryConstraints`, which is used by modules that interact with the player's own inventory (AutoArmor, ChestCleaner, InventoryCleaner, Replenish, Offhand). Modules that interact with external containers (ChestStealer, AutoTool) use the base `InventoryConstraints`, which only offers NoMovement and NoRotation.

### Requirements

**NoMovement** — Requires that the player is not moving or jumping. Specifically, it checks that the player's movement input vector is approximately zero (no WASD keys pressed) and that the player is not pressing the jump key. Actions are postponed until the player stands still.

**NoRotation** — Requires that the player's view rotation has not changed since the previous tick. If a rotation is being managed by the rotation manager (e.g. from KillAura or another aiming module), it checks that the managed rotation matches the previously sent rotation. Otherwise, it checks that the player's current yaw and pitch match the values from the last tick. Actions are postponed while the player is actively looking around.

**InventoryOpen** — Requires that the player's inventory screen is considered open before performing actions. The inventory is considered open if the player has the inventory screen visible on their client, or if it has been opened server-side (silently). When this requirement is selected and the inventory is not yet open, the module will attempt to send a silent open-inventory packet via ViaFabricPlus for server versions 1.11.1 and older, which support the client status packet for inventory opening. On newer server versions (1.12+), the server only becomes aware of inventory interaction when a click packet is sent, so no explicit open packet is needed. Regardless of version, a close packet is always sent when actions are completed. When this requirement is not selected, inventory actions are performed without explicitly opening the inventory screen.

---
*Last updated: 2026-02-13*
