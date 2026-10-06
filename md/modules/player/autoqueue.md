## AutoQueue

AutoQueue (also known by its alias *AutoPlay*) automatically queues you into minigame matches and re-queues once each game finishes, so you can grind rounds without manually typing join commands or clicking lobby NPCs. It ships with ready-made presets for popular servers plus a fully configurable Custom mode you can adapt to almost any server.

Choose the profile that matches where you're playing under **Presets**. *HypixelSW* joins Hypixel SkyWars solo games — it watches for the paper item in your hotbar and then sends the `/play` command for the chosen playlist ([the join loop](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autoqueue/presets/AutoQueueHypixelSW.kt#L42-L55)). *GommeDuels* handles GommeHD.net Duels end-to-end (interacting with the Duels NPC, sending win/lose messages, and managing KillAura) and requires your server language to be set to German. *Custom* lets you define your own **Trigger** (what tells the client a match has ended or a lobby is ready) and **Action** (how the client queues again).

In Custom mode the chosen trigger is checked every tick, and when it fires the chosen action runs — optionally waiting for a world change before it looks for the next trigger ([the trigger/action loop](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autoqueue/presets/AutoQueueCustom.kt#L92-L113)). It can also auto-toggle KillAura and Speed so they only run while you're actually in a match. **Pause** halts the whole module while specific screens are open.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Presets | Mode Selector | HypixelSW | HypixelSW, GommeDuels, Custom | Selects which queue profile to run: a ready-made setup for Hypixel SkyWars or GommeHD.net Duels, or a fully Custom configuration. |
| Presets → [HypixelSW] → GameMode | Choice | Normal | Normal, Insane | Which Hypixel SkyWars solo playlist to join (sends `/play solo_normal` or `/play solo_insane`). |
| Presets → [GommeDuels] → WinMessage | Text | — | — | Chat message sent a couple of seconds after you win a Duels match (default "GG, nice try"). |
| Presets → [GommeDuels] → LoseMessage | Text | — | — | Chat message sent a couple of seconds after you lose a Duels match (default "GG, bist wohl besser als ich!"). |
| Presets → [GommeDuels] → ControlKillAura | Toggle | true | — | Lets this preset enable KillAura once a match starts and disable it between matches. |
| Presets → [Custom] → Trigger | Mode Selector | Title | Title, Title, Message, Item, TabHeader, TabFooter | What the Custom preset watches to decide that a new game should be queued. |
| Presets → [Custom] → Trigger → [Title] → Keywords | Editable List | — | — | Fires when an on-screen title contains any of these words (default "Win", "胜利"). |
| Presets → [Custom] → Trigger → [Title] → Keywords | Editable List | — | — | The second Title option matches the subtitle line instead of the main title; fires when the subtitle contains any keyword (default "恭喜"). |
| Presets → [Custom] → Trigger → [Message] → Keywords | Editable List | — | — | Fires when a received chat message contains any of these words (default "Новая игра", "游戏结束"). |
| Presets → [Custom] → Trigger → [Message] → ChatTypes | Multi-Select | [GameMessage] | ChatMessage, DisguisedChatMessage, GameMessage | Which chat channels the Message trigger listens to (at least one must be selected). |
| Presets → [Custom] → Trigger → [Item] → Mode | Mode Selector | Name | Name, Item | How to identify the trigger item: by display name or by item type. |
| Presets → [Custom] → Trigger → [Item] → Mode → [Name] → Names | Editable List | — | — | Item names to look for in your hotbar or offhand. |
| Presets → [Custom] → Trigger → [Item] → Mode → [Name] → Mode | Choice | Equals | Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase | How a name is compared against the item's display name. |
| Presets → [Custom] → Trigger → [Item] → Mode → [Item] → Items | Registry List | — | — | Item types to look for in your hotbar or offhand. |
| Presets → [Custom] → Trigger → [TabHeader] → Text | Text | — | — | Fires when the tab-list header contains this text (default "Duels"). |
| Presets → [Custom] → Trigger → [TabFooter] → Text | Text | — | — | Fires when the tab-list footer contains this text (default "Duels"). |
| Presets → [Custom] → Action | Mode Selector | Chat | Chat, UseItem | What the Custom preset does to re-queue once the trigger fires. |
| Presets → [Custom] → Action → [Chat] → StartDelay | Integer Range | 0..0 | 0..5000 | Random delay (ms) before the first message is sent. |
| Presets → [Custom] → Action → [Chat] → MessageDelay | Integer Range | 0..0 | 0..5000 | Random delay (ms) between each subsequent message. |
| Presets → [Custom] → Action → [Chat] → Messages | Editable List | — | — | Chat messages or commands sent in order to queue (default "/play solo_normal"). |
| Presets → [Custom] → Action → [UseItem] → Mode | Mode Selector | Name | Name, Item | How to find the item to use: by display name or by item type. |
| Presets → [Custom] → Action → [UseItem] → Mode → [Name] → Names | Editable List | — | — | Item names to search for in your hotbar or offhand. |
| Presets → [Custom] → Action → [UseItem] → Mode → [Name] → Mode | Choice | Equals | Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase | How a name is compared against the item's display name. |
| Presets → [Custom] → Action → [UseItem] → Mode → [Item] → Items | Registry List | — | — | Item types to search for in your hotbar or offhand. |
| Presets → [Custom] → Control | Toggleable Group | on | — | When on, automatically disables the modules below while AutoQueue is queuing and re-enables them afterwards, so they don't run in the lobby. |
| Presets → [Custom] → Control → KillAura | Toggle | true | — | Whether KillAura is included in Control's auto-toggling. |
| Presets → [Custom] → Control → Speed | Toggle | false | — | Whether Speed is included in Control's auto-toggling. |
| Presets → [Custom] → WaitUntilWorldChange | Toggle | true | — | After running the action, wait for a world/server change before watching for the trigger again. |
| Pause | Multi-Select | [ClickGuiOpen, ChatScreenOpen, ContainerScreenOpen, PauseScreenOpen] | ClickGuiOpen, ChatScreenOpen, ContainerScreenOpen, PauseScreenOpen | Screens that fully pause AutoQueue while they are open (ClickGUI, chat box, container/inventory, or the pause menu). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autoqueue/ModuleAutoQueue.kt)*
