## Inventory

Controls how modules that move items, like [ChestStealer](/docs/modules/player/cheststealer) and [InventoryCleaner](/docs/modules/player/inventorycleaner), deal with a server that answers late or puts a clicked item back where it was.

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ResponseTime | Integer | 400 | 50..2000 ms | How long the server gets to answer, for example to open a chest or to put a clicked item back. Clicks wait this long when the answer could still change what they do. |
| LockAfterRejections | Integer | 3 | 1..10 | How often the server may put an item back before modules leave that item alone until you join the next world. |

---

*Last updated: 2026-11-20, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/master/src/main/kotlin/net/ccbluex/liquidbounce/features/global/GlobalSettingsInventory.kt)*
