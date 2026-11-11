## LogoffSpot

When a player you can see leaves the server, LogoffSpot leaves a copy of them standing where they were. The copy shows their armor, items and health from the moment they left.

The copy goes away when its chunk unloads or when the player joins again. You cannot hit the copy.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| SendInChat | Toggle | true | | Writes a chat message when a player leaves, when their copy unloads, and when they come back. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleLogoffSpot.kt)*
