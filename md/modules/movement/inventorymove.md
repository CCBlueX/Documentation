## InventoryMove

InventoryMove lets you walk, jump and sneak while your inventory or a chest is open. Normally you stand still as soon as a menu opens.

Behavior sets how careful it is. Normal lets you move in every menu. Safe lets you move in your own inventory but not in chests or other containers. When you start walking it tells the server your inventory is closed, and it blocks inventory clicks while you move. Undetectable only lets you move in menus that are not containers, so not in your inventory or chests. StopOnAction lets you move everywhere but stops you for a moment each time you click in a menu, so you never click and move at the same time.

You never move while typing in a text box, such as chat, a sign or the ClickGUI search bar. Only the walk, jump, sprint and sneak keys work through menus. Sneak is off unless you turn on PassthroughSneak.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Behavior | Choice | Normal | Normal, Safe, Undetectable, StopOnAction | Which menus you can move in and how careful it is. |
| PassthroughSneak | Toggle | false | | Lets the sneak key work while a menu is open. |
| SprintControl | Toggleable Group | off | | Changes sprinting while a menu is open. |
| SprintControl → Client | Choice | DoNotChange | DoNotChange, ForceSprint, ForceNoSprint | Sprinting on your side. |
| SprintControl → Server | Choice | DoNotChange | DoNotChange, ForceSprint, ForceNoSprint | Sprinting as the server sees it. |
| SneakControl | Toggleable Group | off | | Changes sneaking while a menu is open. |
| SneakControl → Client | Choice | DoNotChange | DoNotChange, ForceSneak, ForceNoSneak | Forces sneaking on or off. |
| Timer | Toggleable Group | off | | Changes game speed while a menu is open. |
| Timer → Speed | Decimal | 1.0 | 0.1..2.0 | Game speed. Above 1.0 is faster, below 1.0 is slower. |
| Blink | Toggleable Group | off | | Holds back your movement while a menu is open and sends it when you close the menu, like [Blink](/docs/modules/player/blink). |
| Blink → MaximumTime | Integer | 10000 | 0..30000 ms | After this many milliseconds the menu closes and the held movement is sent. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/inventorymove/ModuleInventoryMove.kt)*
