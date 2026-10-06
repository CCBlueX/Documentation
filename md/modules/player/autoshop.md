## AutoShop

AutoShop automatically buys items for you in a BedWars shop. Pick a server preset that matches where you're playing, define what gear you want (preset configs ship with the client), and whenever you open the shop villager, AutoShop walks through your buy list and clicks the right category and item slots for you. It only acts while a shop screen that matches the selected preset is open — it [detects the shop by its window title](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autoshop/ModuleAutoShop.kt#L457-L466), so it won't fire on regular containers.

Under the hood it reads your inventory every tick, figures out which configured items you still need and can afford, and only buys what your resources allow — it computes [how many clicks each purchase needs](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autoshop/ModuleAutoShop.kt#L429-L447) and skips items you already own or could replace with a better tier. After every click it [waits until the server actually delivers the items](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autoshop/ModuleAutoShop.kt#L290-L314) before moving on, which keeps it reliable even with server lag.

Use it to instantly restock blocks, tools, armor and potions at the start of a round or after a death, instead of clicking through menus by hand. The two purchase modes trade safety for speed: **Normal** buys one item per click with tick-based delays, while **Quick** batches all affordable purchases in a category with short millisecond delays for much faster shopping.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Config | Choice | PikaNetwork | PikaNetwork, BlocksMC, CubeCraft, TeamHoly, FunnyMC, Dexland | Which server's bundled shop layout and buy list to use. Changing it reloads the matching preset and shows a notification on success or failure. |
| StartDelay | Integer Range | 1..2 | 0..10 | Ticks to wait after the shop opens before the first click, picked at random from the range. Gives the menu time to fully load. |
| PurchaseMode | Mode Selector | Normal | Normal, Quick | How items are bought: one click at a time (Normal) or all affordable items in a category batched together (Quick). |
| PurchaseMode → [Normal] → ExtraDelay | Integer Range | 2..3 | 0..10 | Extra ticks to wait after each individual purchase, picked at random from the range. Higher values are safer against lag. |
| PurchaseMode → [Normal] → Action | Choice | PickUp | PickUp, Throw | The container click type used to trigger a purchase — a normal pick-up click or a throw click, depending on what the server expects. |
| PurchaseMode → [Quick] → Delay | Integer Range | 50..70 | 0..150 | Milliseconds to wait between clicks when batch-buying, picked at random from the range. Lower is faster but riskier. |
| PurchaseMode → [Quick] → WaitForItems | Toggle | true | — | When on, only armor purchases are tracked as pending; the module relies on inventory updates to confirm other items arrived before continuing. When off, all expected items are added as pending up front for faster chaining. |
| ExtraCategorySwitchDelay | Integer Range | 3..4 | 0..10 | Extra ticks to wait after switching shop categories, picked at random from the range. Lets the new category's items load before clicking. |
| AutoClose | Toggle | true | — | Automatically closes the shop after at least one item has been bought, so you can get back into the game quickly. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autoshop/ModuleAutoShop.kt)*
