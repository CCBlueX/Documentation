## BlinkManager

Some modules, like [Blink](/docs/modules/player/blink) and [FakeLag](/docs/modules/combat/fakelag), hold back your movement for a moment so the server still thinks you are where you were. These settings choose how that spot is drawn for you, so you can see where the server thinks you are.

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Esp | Mode Selector | Wireframe | Box, Model, Wireframe, None | How your held-back position is drawn. You only see it in third person. None draws nothing. |
| Esp → [Box] → Color | Color | `#242093`, 34% opacity | | Fill color of the box. |
| Esp → [Box] → OutlineColor | Color | `#242093` | | Outline color of the box. |
| Esp → [Model] → OutlineColor | Color | `#242093`, fully transparent (off) | | Outline color around the player model. |
| Esp → [Model] → LightPercent | Integer | 60% | 0% to 100% | How brightly the player model is lit. |
| Esp → [Wireframe] → Color | Color | `#242093`, 34% opacity | | Fill color of the wireframe player. |
| Esp → [Wireframe] → OutlineColor | Color | `#242093` | | Line color of the wireframe player. |
| Line | Color | `#4677FF` | | Color of the line along the path you moved while held back. |

Your held-back movement is sent all at once when the module lets go. It is also sent when the server teleports you and when you die or respawn. Chat messages are never held back.

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/blink/BlinkManager.kt)*
