## Macros

Macros lets you bind keyboard keys to automated actions so you can trigger them instantly without typing or scrolling through your hotbar. You have five **chat macros** (Chat-1 through Chat-5) and five **item macros** (Item-1 through Item-5), each with its own independent trigger key and configuration.

Chat macros send an ordered list of messages the moment their trigger key is pressed. Messages can be plain chat, server commands (e.g. `/kit pvp`), or LiquidBounce client commands when **UseClientCommand** is on and the message begins with the client prefix. A configurable **Delay** range lets you spread the messages out so they don't all arrive simultaneously. If you want messages sent on a timer instead of a keypress, consider [Spammer](/docs/modules/misc/spammer).

Item macros silently select a matching item from your hotbar or offhand and use it without visibly switching your slot. You can locate the target item either by its display name (with flexible string-matching options) or by item type. The **Action** setting controls whether the item is simply used (`UseOnly`) or placed against a block surface when your crosshair is pointing at one (`PlaceOrUse`). **SwingMode** lets you hide the arm-swing animation from yourself, the server, or both, and **HoldTime** sets how long (in ticks) the slot stays selected before reverting.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Chat-1 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Minimum cooldown between consecutive triggers; a value is randomly sampled from this range each time the macro fires. |
| Chat-1 → Trigger | Key | — | — | The key that activates this chat macro. |
| Chat-1 → Delay | Integer Range | 0..0 | 0..5000 ms | Random delay inserted between each message in the list when sending them in sequence. |
| Chat-1 → Messages | Editable List | — | — | Ordered list of chat messages or commands to send when the macro fires. |
| Chat-1 → UseClientCommand | Toggle | false | — | When enabled, messages starting with the client command prefix are run as LiquidBounce commands instead of being sent to the server. |
| Chat-2 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Minimum cooldown between consecutive triggers; a value is randomly sampled from this range each time the macro fires. |
| Chat-2 → Trigger | Key | — | — | The key that activates this chat macro. |
| Chat-2 → Delay | Integer Range | 0..0 | 0..5000 ms | Random delay inserted between each message in the list when sending them in sequence. |
| Chat-2 → Messages | Editable List | — | — | Ordered list of chat messages or commands to send when the macro fires. |
| Chat-2 → UseClientCommand | Toggle | false | — | When enabled, messages starting with the client command prefix are run as LiquidBounce commands instead of being sent to the server. |
| Chat-3 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Minimum cooldown between consecutive triggers; a value is randomly sampled from this range each time the macro fires. |
| Chat-3 → Trigger | Key | — | — | The key that activates this chat macro. |
| Chat-3 → Delay | Integer Range | 0..0 | 0..5000 ms | Random delay inserted between each message in the list when sending them in sequence. |
| Chat-3 → Messages | Editable List | — | — | Ordered list of chat messages or commands to send when the macro fires. |
| Chat-3 → UseClientCommand | Toggle | false | — | When enabled, messages starting with the client command prefix are run as LiquidBounce commands instead of being sent to the server. |
| Chat-4 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Minimum cooldown between consecutive triggers; a value is randomly sampled from this range each time the macro fires. |
| Chat-4 → Trigger | Key | — | — | The key that activates this chat macro. |
| Chat-4 → Delay | Integer Range | 0..0 | 0..5000 ms | Random delay inserted between each message in the list when sending them in sequence. |
| Chat-4 → Messages | Editable List | — | — | Ordered list of chat messages or commands to send when the macro fires. |
| Chat-4 → UseClientCommand | Toggle | false | — | When enabled, messages starting with the client command prefix are run as LiquidBounce commands instead of being sent to the server. |
| Chat-5 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Minimum cooldown between consecutive triggers; a value is randomly sampled from this range each time the macro fires. |
| Chat-5 → Trigger | Key | — | — | The key that activates this chat macro. |
| Chat-5 → Delay | Integer Range | 0..0 | 0..5000 ms | Random delay inserted between each message in the list when sending them in sequence. |
| Chat-5 → Messages | Editable List | — | — | Ordered list of chat messages or commands to send when the macro fires. |
| Chat-5 → UseClientCommand | Toggle | false | — | When enabled, messages starting with the client command prefix are run as LiquidBounce commands instead of being sent to the server. |
| Item-1 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Minimum cooldown between consecutive triggers; a value is randomly sampled from this range each time the macro fires. |
| Item-1 → Trigger | Key | — | — | The key that activates this item macro. |
| Item-1 → Action | Choice | UseOnly | — | `UseOnly` right-click-uses the item (e.g. drinks a potion, charges a bow). `PlaceOrUse` places the item as a block if the crosshair is over a surface, otherwise uses it. |
| Item-1 → PickMode | Mode Selector | Name | — | How to find the target item in your hotbar or offhand: by display name (`Name`) or by item type (`Item`). |
| Item-1 → PickMode → \[Mode: Name\] → Names | Editable List | — | — | Display names to search for when PickMode is Name. |
| Item-1 → PickMode → \[Mode: Name\] → Mode | Choice | Equals | — | String-matching strategy for comparing item names: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, or `EndsWithIgnoreCase`. |
| Item-1 → PickMode → \[Mode: Item\] → Items | Registry List | — | — | Item types to match against when PickMode is Item. |
| Item-1 → SwingMode | Choice | DoNotHide | — | Whether to suppress the arm-swing animation. `DoNotHide` shows it normally; `HideForBoth` hides it client- and server-side; `HideForClient` hides it only on your screen; `HideForServer` omits it from the server packet. |
| Item-1 → HoldTime | Integer Range | 1..1 | 1..20 ticks | How many ticks the macro holds the selected slot before reverting to your original slot. |
| Item-2 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Minimum cooldown between consecutive triggers; a value is randomly sampled from this range each time the macro fires. |
| Item-2 → Trigger | Key | — | — | The key that activates this item macro. |
| Item-2 → Action | Choice | UseOnly | — | `UseOnly` right-click-uses the item. `PlaceOrUse` places the item as a block if the crosshair is over a surface, otherwise uses it. |
| Item-2 → PickMode | Mode Selector | Name | — | How to find the target item in your hotbar or offhand: by display name (`Name`) or by item type (`Item`). |
| Item-2 → PickMode → \[Mode: Name\] → Names | Editable List | — | — | Display names to search for when PickMode is Name. |
| Item-2 → PickMode → \[Mode: Name\] → Mode | Choice | Equals | — | String-matching strategy for comparing item names: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, or `EndsWithIgnoreCase`. |
| Item-2 → PickMode → \[Mode: Item\] → Items | Registry List | — | — | Item types to match against when PickMode is Item. |
| Item-2 → SwingMode | Choice | DoNotHide | — | Whether to suppress the arm-swing animation. `DoNotHide` shows it normally; `HideForBoth` hides it client- and server-side; `HideForClient` hides it only on your screen; `HideForServer` omits it from the server packet. |
| Item-2 → HoldTime | Integer Range | 1..1 | 1..20 ticks | How many ticks the macro holds the selected slot before reverting to your original slot. |
| Item-3 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Minimum cooldown between consecutive triggers; a value is randomly sampled from this range each time the macro fires. |
| Item-3 → Trigger | Key | — | — | The key that activates this item macro. |
| Item-3 → Action | Choice | UseOnly | — | `UseOnly` right-click-uses the item. `PlaceOrUse` places the item as a block if the crosshair is over a surface, otherwise uses it. |
| Item-3 → PickMode | Mode Selector | Name | — | How to find the target item in your hotbar or offhand: by display name (`Name`) or by item type (`Item`). |
| Item-3 → PickMode → \[Mode: Name\] → Names | Editable List | — | — | Display names to search for when PickMode is Name. |
| Item-3 → PickMode → \[Mode: Name\] → Mode | Choice | Equals | — | String-matching strategy for comparing item names: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, or `EndsWithIgnoreCase`. |
| Item-3 → PickMode → \[Mode: Item\] → Items | Registry List | — | — | Item types to match against when PickMode is Item. |
| Item-3 → SwingMode | Choice | DoNotHide | — | Whether to suppress the arm-swing animation. `DoNotHide` shows it normally; `HideForBoth` hides it client- and server-side; `HideForClient` hides it only on your screen; `HideForServer` omits it from the server packet. |
| Item-3 → HoldTime | Integer Range | 1..1 | 1..20 ticks | How many ticks the macro holds the selected slot before reverting to your original slot. |
| Item-4 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Minimum cooldown between consecutive triggers; a value is randomly sampled from this range each time the macro fires. |
| Item-4 → Trigger | Key | — | — | The key that activates this item macro. |
| Item-4 → Action | Choice | UseOnly | — | `UseOnly` right-click-uses the item. `PlaceOrUse` places the item as a block if the crosshair is over a surface, otherwise uses it. |
| Item-4 → PickMode | Mode Selector | Name | — | How to find the target item in your hotbar or offhand: by display name (`Name`) or by item type (`Item`). |
| Item-4 → PickMode → \[Mode: Name\] → Names | Editable List | — | — | Display names to search for when PickMode is Name. |
| Item-4 → PickMode → \[Mode: Name\] → Mode | Choice | Equals | — | String-matching strategy for comparing item names: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, or `EndsWithIgnoreCase`. |
| Item-4 → PickMode → \[Mode: Item\] → Items | Registry List | — | — | Item types to match against when PickMode is Item. |
| Item-4 → SwingMode | Choice | DoNotHide | — | Whether to suppress the arm-swing animation. `DoNotHide` shows it normally; `HideForBoth` hides it client- and server-side; `HideForClient` hides it only on your screen; `HideForServer` omits it from the server packet. |
| Item-4 → HoldTime | Integer Range | 1..1 | 1..20 ticks | How many ticks the macro holds the selected slot before reverting to your original slot. |
| Item-5 → TriggerDelay | Integer Range | 0..0 | 0..15000 ms | Minimum cooldown between consecutive triggers; a value is randomly sampled from this range each time the macro fires. |
| Item-5 → Trigger | Key | — | — | The key that activates this item macro. |
| Item-5 → Action | Choice | UseOnly | — | `UseOnly` right-click-uses the item. `PlaceOrUse` places the item as a block if the crosshair is over a surface, otherwise uses it. |
| Item-5 → PickMode | Mode Selector | Name | — | How to find the target item in your hotbar or offhand: by display name (`Name`) or by item type (`Item`). |
| Item-5 → PickMode → \[Mode: Name\] → Names | Editable List | — | — | Display names to search for when PickMode is Name. |
| Item-5 → PickMode → \[Mode: Name\] → Mode | Choice | Equals | — | String-matching strategy for comparing item names: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, or `EndsWithIgnoreCase`. |
| Item-5 → PickMode → \[Mode: Item\] → Items | Registry List | — | — | Item types to match against when PickMode is Item. |
| Item-5 → SwingMode | Choice | DoNotHide | — | Whether to suppress the arm-swing animation. `DoNotHide` shows it normally; `HideForBoth` hides it client- and server-side; `HideForClient` hides it only on your screen; `HideForServer` omits it from the server packet. |
| Item-5 → HoldTime | Integer Range | 1..1 | 1..20 ticks | How many ticks the macro holds the selected slot before reverting to your original slot. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleMacros.kt)*
