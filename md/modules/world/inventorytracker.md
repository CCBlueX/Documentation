## InventoryTracker

InventoryTracker quietly watches the gear and items other players reveal during a match and remembers them for you. Whenever an enemy swaps weapons, equips armor, or pulls something out of their offhand, that item is recorded and added to a reconstructed snapshot of their inventory. This lets you build up a picture of what an opponent is carrying over the course of a fight, even though you never actually opened their inventory.

To review what has been tracked, use the `.invsee` command to open a viewer for a specific player. Each item in the viewer shows a "Last Seen" timestamp, so you can tell how recently they had a given weapon or piece of armor in hand. This is handy for scouting threats — knowing whether someone still has a powerful sword, a totem, or fresh armor before you commit to a push. Bots flagged by [AntiBot](/docs/modules/misc/antibot) are ignored so you only track real players.

By default, tracking only works for players currently within your render distance. Enabling **SavePlayers** keeps a reference to each tracked player so you can still look up their recorded inventory after they move out of range. The collected data is cleared automatically when you change worlds or disable the module.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| SavePlayers | Toggle | false | — | Keeps tracked players in memory so their recorded inventories can still be viewed even after they leave your render distance. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleInventoryTracker.kt)*
