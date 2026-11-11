## Macros

Macros run actions with one key press. There are five chat macros (Chat-1 to Chat-5) and five item macros (Item-1 to Item-5), each with its own key.

A chat macro sends a list of messages, like `/kit pvp`, one after another. An item macro finds an item in your hotbar or offhand and uses it, then switches back to the slot you had. To send messages on a timer instead, use [Spammer](/docs/modules/misc/spammer).

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Chat-1 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Shortest wait before the macro can run again. |
| Chat-1 → Trigger | Key | | | Key that runs the macro. |
| Chat-1 → Delay | Integer Range | 0..0 | 0..5000 ms | Wait between messages. |
| Chat-1 → Messages | Editable List | | | Messages and commands to send, in order. |
| Chat-1 → UseClientCommand | Toggle | false | | Runs messages that start with the client prefix (`.`) as LiquidBounce commands. |
| Chat-2 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Shortest wait before the macro can run again. |
| Chat-2 → Trigger | Key | | | Key that runs the macro. |
| Chat-2 → Delay | Integer Range | 0..0 | 0..5000 ms | Wait between messages. |
| Chat-2 → Messages | Editable List | | | Messages and commands to send, in order. |
| Chat-2 → UseClientCommand | Toggle | false | | Runs messages that start with the client prefix (`.`) as LiquidBounce commands. |
| Chat-3 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Shortest wait before the macro can run again. |
| Chat-3 → Trigger | Key | | | Key that runs the macro. |
| Chat-3 → Delay | Integer Range | 0..0 | 0..5000 ms | Wait between messages. |
| Chat-3 → Messages | Editable List | | | Messages and commands to send, in order. |
| Chat-3 → UseClientCommand | Toggle | false | | Runs messages that start with the client prefix (`.`) as LiquidBounce commands. |
| Chat-4 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Shortest wait before the macro can run again. |
| Chat-4 → Trigger | Key | | | Key that runs the macro. |
| Chat-4 → Delay | Integer Range | 0..0 | 0..5000 ms | Wait between messages. |
| Chat-4 → Messages | Editable List | | | Messages and commands to send, in order. |
| Chat-4 → UseClientCommand | Toggle | false | | Runs messages that start with the client prefix (`.`) as LiquidBounce commands. |
| Chat-5 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Shortest wait before the macro can run again. |
| Chat-5 → Trigger | Key | | | Key that runs the macro. |
| Chat-5 → Delay | Integer Range | 0..0 | 0..5000 ms | Wait between messages. |
| Chat-5 → Messages | Editable List | | | Messages and commands to send, in order. |
| Chat-5 → UseClientCommand | Toggle | false | | Runs messages that start with the client prefix (`.`) as LiquidBounce commands. |
| Item-1 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Shortest wait before the macro can run again. |
| Item-1 → Trigger | Key | | | Key that runs the macro. |
| Item-1 → Action | Choice | UseOnly | UseOnly, PlaceOrUse | UseOnly uses the item. PlaceOrUse places it as a block if you look at one, and uses it otherwise. |
| Item-1 → PickMode | Mode Selector | Name | Name, Item | Find the item by its name or by its type. |
| Item-1 → PickMode → [Name] → Names | Editable List | Paper | | Item names to look for. |
| Item-1 → PickMode → [Name] → Mode | Choice | Equals | Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase | How the name has to match. |
| Item-1 → PickMode → [Item] → Items | Registry List | Paper | | Item types to look for. |
| Item-1 → SwingMode | Choice | DoNotHide | DoNotHide, HideForClient | HideForClient hides your arm swing on your own screen. |
| Item-1 → HoldTime | Integer Range | 1..1 | 1..20 ticks | How long the item stays selected before you switch back, in ticks (20 per second). |
| Item-2 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Shortest wait before the macro can run again. |
| Item-2 → Trigger | Key | | | Key that runs the macro. |
| Item-2 → Action | Choice | UseOnly | UseOnly, PlaceOrUse | UseOnly uses the item. PlaceOrUse places it as a block if you look at one, and uses it otherwise. |
| Item-2 → PickMode | Mode Selector | Name | Name, Item | Find the item by its name or by its type. |
| Item-2 → PickMode → [Name] → Names | Editable List | Paper | | Item names to look for. |
| Item-2 → PickMode → [Name] → Mode | Choice | Equals | Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase | How the name has to match. |
| Item-2 → PickMode → [Item] → Items | Registry List | Paper | | Item types to look for. |
| Item-2 → SwingMode | Choice | DoNotHide | DoNotHide, HideForClient | HideForClient hides your arm swing on your own screen. |
| Item-2 → HoldTime | Integer Range | 1..1 | 1..20 ticks | How long the item stays selected before you switch back, in ticks (20 per second). |
| Item-3 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Shortest wait before the macro can run again. |
| Item-3 → Trigger | Key | | | Key that runs the macro. |
| Item-3 → Action | Choice | UseOnly | UseOnly, PlaceOrUse | UseOnly uses the item. PlaceOrUse places it as a block if you look at one, and uses it otherwise. |
| Item-3 → PickMode | Mode Selector | Name | Name, Item | Find the item by its name or by its type. |
| Item-3 → PickMode → [Name] → Names | Editable List | Paper | | Item names to look for. |
| Item-3 → PickMode → [Name] → Mode | Choice | Equals | Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase | How the name has to match. |
| Item-3 → PickMode → [Item] → Items | Registry List | Paper | | Item types to look for. |
| Item-3 → SwingMode | Choice | DoNotHide | DoNotHide, HideForClient | HideForClient hides your arm swing on your own screen. |
| Item-3 → HoldTime | Integer Range | 1..1 | 1..20 ticks | How long the item stays selected before you switch back, in ticks (20 per second). |
| Item-4 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Shortest wait before the macro can run again. |
| Item-4 → Trigger | Key | | | Key that runs the macro. |
| Item-4 → Action | Choice | UseOnly | UseOnly, PlaceOrUse | UseOnly uses the item. PlaceOrUse places it as a block if you look at one, and uses it otherwise. |
| Item-4 → PickMode | Mode Selector | Name | Name, Item | Find the item by its name or by its type. |
| Item-4 → PickMode → [Name] → Names | Editable List | Paper | | Item names to look for. |
| Item-4 → PickMode → [Name] → Mode | Choice | Equals | Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase | How the name has to match. |
| Item-4 → PickMode → [Item] → Items | Registry List | Paper | | Item types to look for. |
| Item-4 → SwingMode | Choice | DoNotHide | DoNotHide, HideForClient | HideForClient hides your arm swing on your own screen. |
| Item-4 → HoldTime | Integer Range | 1..1 | 1..20 ticks | How long the item stays selected before you switch back, in ticks (20 per second). |
| Item-5 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Shortest wait before the macro can run again. |
| Item-5 → Trigger | Key | | | Key that runs the macro. |
| Item-5 → Action | Choice | UseOnly | UseOnly, PlaceOrUse | UseOnly uses the item. PlaceOrUse places it as a block if you look at one, and uses it otherwise. |
| Item-5 → PickMode | Mode Selector | Name | Name, Item | Find the item by its name or by its type. |
| Item-5 → PickMode → [Name] → Names | Editable List | Paper | | Item names to look for. |
| Item-5 → PickMode → [Name] → Mode | Choice | Equals | Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase | How the name has to match. |
| Item-5 → PickMode → [Item] → Items | Registry List | Paper | | Item types to look for. |
| Item-5 → SwingMode | Choice | DoNotHide | DoNotHide, HideForClient | HideForClient hides your arm swing on your own screen. |
| Item-5 → HoldTime | Integer Range | 1..1 | 1..20 ticks | How long the item stays selected before you switch back, in ticks (20 per second). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleMacros.kt)*
