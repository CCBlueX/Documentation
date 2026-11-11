## FlagCheck

When the server thinks you moved in a way you shouldn't, it pulls you back or turns your head. Players call this a "flag" or "lagback". FlagCheck counts these and tells you each time, so you can see how often the anti-cheat catches you. It can also draw a box where the server put you back.

It never changes how you move. Use it to test modules like [Speed](/docs/modules/movement/speed) or [Fly](/docs/modules/movement/fly) on a server.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ChatMessage | Toggle | true | | Writes a chat message for each flag. |
| Notification | Toggle | false | | Shows a notification for each flag. |
| InvalidAttributes | Toggle | false | | Also warns when your health or hunger is zero while you are still alive. |
| ResetFlags | Toggleable Group | On | | Sets the counter back to zero after a while without flags. |
| ResetFlags → After | Integer | 30 | 1..300 s | How long without flags before the counter resets. |
| Render | Toggleable Group | On | | Draws a box where the server put you back. |
| Render → NotInFirstPerson | Toggle | true | | Only draws the box when you are not in first-person view. |
| Render → Alive | Integer | 1000 | 0..3000 ms | How long the box stays before it fades. |
| Render → FadeOut | Choice | QuadOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the box fades away. |
| Render → OutTime | Integer | 500 | 0..2000 ms | How long the fading takes. |
| Render → Color | Color | | | Fill color of the box. |
| Render → OutlineColor | Color | | | Outline color of the box. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleFlagCheck.kt)*
