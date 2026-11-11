## Blink

Blink stops sending your movement to the server while it is on. To other players you stand still where you turned it on, while you keep walking on your screen. When you turn it off, everything is sent at once and you seem to teleport to where you really are. Use it to get away from a fight or to sneak up on someone.

With [AutoDodge](/docs/modules/combat/autododge) on, Blink also lets just enough movement through to dodge arrows flying at you.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Directions | Multi-Select | Outgoing | Incoming, Outgoing | What to hold back. Outgoing holds what you send to the server, Incoming holds what the server sends to you. At least one must be on. |
| Dummy | Toggle | false | | Shows a copy of you where the server still thinks you are. |
| Ambush | Toggle | false | | Turns Blink off as soon as you hit or use an entity, so your hit lands from where you really are. |
| AutoDisable | Toggle | true | | Turns Blink off after AutoReset. |
| AutoReset | Toggleable Group | Off | | Ends the blink by itself after a while. |
| AutoReset → ResetAfter | Integer | 100 | 1..1000 | How long to wait, in ticks (20 per second). |
| AutoReset → ResetAction | Choice | Reset | Reset, Blink | Reset throws away the held movement and puts you back where you started. Blink sends it, so you teleport forward. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleBlink.kt)*
