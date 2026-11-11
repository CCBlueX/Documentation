## AutoQueue

AutoQueue joins a new game for you every time a minigame round ends, so you can keep playing round after round without typing commands or clicking NPCs. It has ready setups for some servers and a Custom mode you can set up for others.

**Presets** picks the setup:

- **HypixelSW** joins Hypixel SkyWars solo games when the paper item shows up in your hotbar.
- **GommeDuels** joins Duels on GommeHD.net through the Duels NPC and sends a chat message after each match. Your server language must be German.
- **Custom** waits for something you choose (**Trigger**), like a title or a chat message, and then does something you choose (**Action**), like sending a command.

**Category:** Player
**Enabled by default:** No
**Aliases:** AutoPlay

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Presets | Mode Selector | HypixelSW | HypixelSW, GommeDuels, Custom | Which setup to use. |
| Presets → [HypixelSW] → GameMode | Choice | Normal | Normal, Insane | Which SkyWars solo mode to join. |
| Presets → [GommeDuels] → WinMessage | Text | GG, nice try | | Chat message sent after you win. |
| Presets → [GommeDuels] → LoseMessage | Text | GG, bist wohl besser als ich! | | Chat message sent after you lose. |
| Presets → [GommeDuels] → ControlKillAura | Toggle | true | | Turns [KillAura](/docs/modules/combat/killaura) on when a match starts and off between matches. |
| Presets → [Custom] → Trigger | Mode Selector | Title | Title, Title, Message, Item, TabHeader, TabFooter | What tells AutoQueue that it is time to join a new game. The second Title option checks the smaller line under the title. |
| Presets → [Custom] → Trigger → [Title] → Keywords | Text List | Win, 胜利 | | Joins when the big title on screen contains one of these words. |
| Presets → [Custom] → Trigger → [Title (second)] → Keywords | Text List | 恭喜 | | Joins when the line under the title contains one of these words. |
| Presets → [Custom] → Trigger → [Message] → Keywords | Text List | Новая игра, 游戏结束 | | Joins when a chat message contains one of these words. |
| Presets → [Custom] → Trigger → [Message] → ChatTypes | Multi-Select | GameMessage | ChatMessage, DisguisedChatMessage, GameMessage | Which kinds of chat messages to check. |
| Presets → [Custom] → Trigger → [Item] → Mode | Mode Selector | Name | Name, Item | Find the item by its name or by its item type. |
| Presets → [Custom] → Trigger → [Item] → Mode → [Name] → Names | Text List | Paper | | Item names to look for in your hotbar or offhand. |
| Presets → [Custom] → Trigger → [Item] → Mode → [Name] → Mode | Choice | Equals | Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase | How the name has to match. |
| Presets → [Custom] → Trigger → [Item] → Mode → [Item] → Items | Registry List | Paper | | Item types to look for in your hotbar or offhand. |
| Presets → [Custom] → Trigger → [TabHeader] → Text | Text | Duels | | Joins when the top of the tab list contains this text. |
| Presets → [Custom] → Trigger → [TabFooter] → Text | Text | Duels | | Joins when the bottom of the tab list contains this text. |
| Presets → [Custom] → Action | Mode Selector | Chat | Chat, UseItem | What to do to join a new game. |
| Presets → [Custom] → Action → [Chat] → StartDelay | Integer Range | 0..0 | 0..5000 ms | Wait before the first message. |
| Presets → [Custom] → Action → [Chat] → MessageDelay | Integer Range | 0..0 | 0..5000 ms | Wait between messages. |
| Presets → [Custom] → Action → [Chat] → Messages | Text List | /play solo_normal | | Messages or commands to send, in order. |
| Presets → [Custom] → Action → [UseItem] → Mode | Mode Selector | Name | Name, Item | Find the item by its name or by its item type. |
| Presets → [Custom] → Action → [UseItem] → Mode → [Name] → Names | Text List | Paper | | Item names to look for in your hotbar or offhand. |
| Presets → [Custom] → Action → [UseItem] → Mode → [Name] → Mode | Choice | Equals | Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase | How the name has to match. |
| Presets → [Custom] → Action → [UseItem] → Mode → [Item] → Items | Registry List | Paper | | Item types to look for in your hotbar or offhand. |
| Presets → [Custom] → Control | Toggleable Group | On | | Turns the modules below off while you wait for a new game and on again when it starts. |
| Presets → [Custom] → Control → KillAura | Toggle | true | | Do this for [KillAura](/docs/modules/combat/killaura). |
| Presets → [Custom] → Control → Speed | Toggle | false | | Do this for [Speed](/docs/modules/movement/speed). |
| Presets → [Custom] → WaitUntilWorldChange | Toggle | true | | After joining, waits until you are moved to a new world before checking the trigger again. |
| Pause | Multi-Select | ClickGuiOpen, ChatScreenOpen, ContainerScreenOpen, PauseScreenOpen | ClickGuiOpen, ChatScreenOpen, ContainerScreenOpen, PauseScreenOpen | AutoQueue waits while one of these screens is open. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/autoqueue/ModuleAutoQueue.kt)*
