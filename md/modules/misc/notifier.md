## Notifier

Notifier tells you about things that happen on the server: players joining or leaving, game mode changes, players eating or drinking, players holding dangerous items like End Crystals, and totems popping. Turn on only the messages you want and change their text if you like.

Messages go to chat. Turn on UseNotification to get them as pop-up notifications instead. Players that [AntiBot](/docs/modules/misc/antibot) marks as bots are skipped for the eating and held-item messages.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| JoinMessages | Toggle | true | | Tells you when a player joins. |
| JoinMessageFormat | Text | %s joined | | Text of the message. `%s` is the player's name. |
| LeaveMessages | Toggle | true | | Tells you when a player leaves. |
| LeaveMessageFormat | Text | %s left | | Text of the message. `%s` is the player's name. |
| GameModeMessages | Toggle | false | | Tells you when a player's game mode changes. |
| GameModeMessageFormat | Text | %s changed their game mode to %s | | Text of the message. The first `%s` is the player, the second the new game mode. |
| ItemConsumptionMessages | Toggle | true | | Tells you when a player finishes eating or drinking something. |
| ItemConsumptionMessageFormat | Text | %1$s used %2$s | | Text of the message. `%1$s` is the player, `%2$s` the item. |
| HeldItemMessages | Toggle | false | | Tells you when a player holds one of the HeldItems. |
| HeldItemMessageFormat | Text | %1$s holds %2$s x%3$s in %4$s | | Text of the message. `%1$s` is the player, `%2$s` the item, `%3$s` how many, `%4$s` which hand. |
| HeldItems | Registry List | End Crystal, Enchanted Golden Apple | | Items to watch for. |
| TotemPopMessages | Toggle | true | | Tells you when a player uses up a Totem of Undying, and how many they used so far. Skips you and your friends. |
| TotemPopMessageFormat | Text | %1$s popped a totem %2$s times | | Text of the message. `%1$s` is the player, `%2$s` the count. |
| UseNotification | Toggle | false | | Shows messages as notifications instead of in chat. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleNotifier.kt)*
