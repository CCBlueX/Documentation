## InventoryTracker

InventoryTracker remembers the items other players hold and wear. Each time a player shows a new weapon, armor piece or offhand item, it gets added to a list for that player.

Use the `.invsee` command to look at what a player had. Each item shows when you last saw it. Bots found by [AntiBot](/docs/modules/misc/antibot) are skipped. Everything is forgotten when you change worlds or turn the module off.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| SavePlayers | Toggle | false | | Keeps the items of players who left your view, so you can still look them up. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleInventoryTracker.kt)*
