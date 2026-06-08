## FlagCheck

FlagCheck watches for the small position and rotation corrections a server sends when it thinks something is off with your movement — commonly called "flags," "lagbacks," or "setbacks." Whenever the server snaps you back to a different spot or forcibly turns your view, FlagCheck counts it and lets you know, so you can tell at a glance how often a server's anti-cheat is reacting to you. It can also flag impossible states like being alive with zero health or zero hunger.

You can be alerted by chat message, by an on-screen notification, or both. The running flag counter is shown with each alert and automatically clears itself after a set period of quiet (or when you disconnect), so a few old flags don't keep inflating the number. FlagCheck can also draw a wireframe at the exact position and facing the server tried to move you to, which is handy for spotting where and how hard you were corrected.

This is a passive, information-only tool — it never changes your movement. Pair it with modules like [Velocity](/docs/modules/combat/velocity), [Speed](/docs/modules/movement/speed), or [Fly](/docs/modules/movement/fly) to gauge whether a server is silently correcting you.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| ChatMessage | Toggle | true | — | Prints a chat message each time a flag is detected. |
| Notification | Toggle | true | — | Shows an on-screen notification each time a flag is detected. |
| InvalidAttributes | Toggle | true | — | Also flags impossible states, such as being alive with no health or no hunger. |
| ResetFlags | Toggleable Group | on | — | Automatically clears the flag counter after a period without new flags. |
| ResetFlags → After | Integer | 30 | 1..300 (s) | How long to wait with no new flags before the counter resets to zero. |
| Render | Toggleable Group | on | — | Draws a wireframe at the position and facing the server tried to correct you to. |
| Render → NotInFirstPerson | Toggle | true | — | Only shows the wireframe when you are not in first-person view. |
| Render → Alive | Integer | 1000 | 0..3000 (ms) | How long the wireframe stays fully visible before fading out. |
| Render → FadeOut | Choice | QuadOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | Easing curve used as the wireframe fades away. |
| Render → OutTime | Integer | 500 | 0..2000 (ms) | How long the fade-out animation takes. |
| Render → Color | Color | — | — | Fill color of the wireframe. |
| Render → OutlineColor | Color | — | — | Outline color of the wireframe. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleFlagCheck.kt)*
