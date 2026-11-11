## MiddleClickAction

MiddleClickAction gives your middle mouse button a new job. In FriendClicker mode, middle-click a player to add them to your friends, or click again to remove them. In Pearl mode, middle-click throws an ender pearl from your hotbar or offhand without you switching slots.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | FriendClicker | FriendClicker, Pearl | What middle-click does. |
| Mode → [FriendClicker] → PickUpRange | Decimal | 3.0 | 1.0..100.0 | How far away (in blocks) the player can be. |
| Mode → [Pearl] → SlotResetDelay | Integer | 1 | 0..10 ticks | How long to wait before switching back to your slot, in ticks (20 per second). |
| Mode → [Pearl] → StopOnSubmit | Decimal Range | 85.0..90.0 | 60.0..90.0 pitch | Doesn't throw while you look this far down. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleMiddleClickAction.kt)*
