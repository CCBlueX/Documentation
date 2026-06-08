## MiddleClickAction

MiddleClickAction lets you bind useful actions to your middle mouse button (the default "pick block" key). Instead of the usual pick-block behaviour, pressing middle click will trigger one of two configurable actions depending on the selected mode.

In **FriendClicker** mode, middle-clicking while aiming at a player will instantly toggle them as a friend — adding them if they are not already on your friend list, or removing them if they are. A notification confirms the change. This is a quick alternative to opening menus just to manage your friends list mid-game.

In **Pearl** mode, middle-clicking will silently switch to an Ender Pearl in your hotbar or offhand and throw it, then restore your previous slot after a short delay. This gives you a fast, dedicated pearl-throw keybind without interrupting your normal hotbar flow. The throw is cancelled automatically if your pitch reaches the configured `StopOnSubmit` range (useful to avoid misfires when looking straight down).

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | FriendClicker | FriendClicker, Pearl | Selects which action is performed on middle click. |
| Mode → [FriendClicker] → PickUpRange | Decimal | 3.0 | 1.0–100.0 | Maximum distance (in blocks) at which a player can be targeted for friend toggling. |
| Mode → [Pearl] → SlotResetDelay | Integer | 1 | 0–10 ticks | How many ticks to wait before restoring your original hotbar slot after throwing the pearl. |
| Mode → [Pearl] → StopOnSubmit | Decimal Range | 85.0–90.0 | 60.0–90.0 (Pitch) | Pitch range at which the pearl throw is suppressed. Prevents accidental throws when looking straight down. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleMiddleClickAction.kt)*
