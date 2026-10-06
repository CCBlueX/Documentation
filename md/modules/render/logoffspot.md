## LogoffSpot

LogoffSpot tracks the last known position of players who disconnect from the server. When another player logs off while you can see them, the module leaves behind a ghost — a static copy of that player at the exact spot they disappeared — so you always know where they were standing when they left.

The ghost accurately reflects the logged-off player's appearance, equipment, and health at the time of disconnect. It will automatically disappear if the chunk it occupies unloads, or if that player reconnects to the server. When **SendInChat** is enabled, you receive a chat notification each time one of these events happens — when a player disappears, when their ghost unloads with the chunk, and when they come back online. This makes it easy to keep tabs on players even if you aren't watching the screen at that moment.

This module pairs well with [ESP](/docs/modules/render/esp) or [Nametags](/docs/modules/render/nametags) to make the ghost figures easier to spot at a distance. Note that the ghosts are client-side only and cannot be attacked or interacted with; any interaction packets directed at them are silently cancelled so you don't accidentally waste hits.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| SendInChat | Toggle | true | — | When enabled, posts a chat message whenever a player's ghost is created (logged off), removed because their chunk unloaded, or removed because they rejoined the server. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleLogoffSpot.kt)*
