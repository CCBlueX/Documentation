## Notifier

Notifier watches for a range of in-game events and reports them to you either in chat or as brief HUD toast notifications. You can track players joining and leaving the server, catch when someone switches to or finishes using a dangerous item (such as an End Crystal or an Enchanted Golden Apple), detect game-mode changes, and count how many totems an opponent has popped — all without having to watch the chat yourself.

Every event type has its own toggle and a fully customisable format string, so you can enable only the alerts you care about and phrase them however you like. Players that [AntiBot](/docs/modules/misc/antibot) identifies as bots are automatically excluded from per-tick checks (item consumption and held-item tracking), keeping the feed clean on servers that host NPCs or fake players.

When **UseNotification** is off (the default), alerts appear as regular chat messages. Switching it on routes them through the client's notification system instead, displaying them as on-screen toasts that won't clutter your chat history.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| JoinMessages | Toggle | true | — | Send a message whenever a player joins the server. |
| JoinMessageFormat | Text | — | — | Format string for join messages. `%s` is replaced with the joining player's name. |
| LeaveMessages | Toggle | true | — | Send a message whenever a player leaves the server. |
| LeaveMessageFormat | Text | — | — | Format string for leave messages. `%s` is replaced with the leaving player's name. |
| GameModeMessages | Toggle | false | — | Send a message when a player's game mode changes. Does not fire for the initial game mode assigned on join. |
| GameModeMessageFormat | Text | — | — | Format string for game-mode change messages. The first `%s` is the player's name; the second is their new game mode. |
| ItemConsumptionMessages | Toggle | true | — | Send a message when a nearby player finishes eating food or drinking a potion. |
| ItemConsumptionMessageFormat | Text | — | — | Format string for item-consumption messages. `%1$s` is the player's name; `%2$s` is the item name. |
| HeldItemMessages | Toggle | false | — | Send a message when a nearby player holds any item listed in **HeldItems** in their main or off hand. |
| HeldItemMessageFormat | Text | — | — | Format string for held-item messages. `%1$s` = player name, `%2$s` = item name, `%3$s` = stack count, `%4$s` = hand (main or off). |
| HeldItems | Registry List | — | — | The items to watch for when HeldItemMessages is enabled. Defaults to End Crystals and Enchanted Golden Apples. |
| TotemPopMessages | Toggle | true | — | Send a message whenever a player survives with a Totem of Undying, including a running total of how many totems that player has popped this session. Friendly players and yourself are excluded. |
| TotemPopMessageFormat | Text | — | — | Format string for totem-pop messages. `%1$s` is the player's name; `%2$s` is their cumulative pop count. |
| UseNotification | Toggle | false | — | When enabled, all alerts are displayed as HUD toast notifications instead of chat messages. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleNotifier.kt)*
