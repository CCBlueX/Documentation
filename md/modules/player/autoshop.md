## AutoShop

AutoShop buys items for you in the BedWars shop. Pick the server you play on, open the shop villager, and it clicks through the shop and buys the items on its list, as long as you have enough resources. It skips things you already have or have a better version of. Use it to grab blocks, tools, armor and potions fast at the start of a round or after you die.

It only clicks in a shop screen of the server you picked, never in normal chests.

**Category:** Player
**Enabled by default:** No

### Settings

Some settings are in ticks (20 per second).

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Config | Choice | PikaNetwork | PikaNetwork, BlocksMC, CubeCraft, TeamHoly, FunnyMC, Dexland | Which server's shop and buy list to use. |
| StartDelay | Integer Range | 1..2 | 0..10 ticks | Wait after the shop opens before the first click. |
| PurchaseMode | Mode Selector | Normal | Normal, Quick | Normal buys one item at a time. Quick buys everything in a shop page in one go, which is faster. |
| PurchaseMode → [Normal] → ExtraDelay | Integer Range | 2..3 | 0..10 ticks | Extra wait after each purchase. Higher is safer when the server lags. |
| PurchaseMode → [Normal] → Action | Choice | PickUp | PickUp, Throw | Which kind of click buys an item. Change it if the server expects a different click. |
| PurchaseMode → [Quick] → Delay | Integer Range | 50..70 | 0..150 ms | Wait between clicks. Lower is faster but riskier. |
| PurchaseMode → [Quick] → WaitForItems | Toggle | true | | Changes how it waits for bought items to show up in your inventory before buying more. |
| ExtraCategorySwitchDelay | Integer Range | 3..4 | 0..10 ticks | Extra wait after switching to another shop page. |
| AutoClose | Toggle | true | | Closes the shop after it bought something. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autoshop/ModuleAutoShop.kt)*
