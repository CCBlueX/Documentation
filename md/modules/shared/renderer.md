## Renderer

The Renderer settings decide how often the client's own screens are drawn, like the ClickGUI and the HUD. Lower values can help on slow computers.

Used by: [ClickGUI](/docs/modules/render/clickgui), [HUD](/docs/modules/render/hud).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Fps | Integer | 0 (ClickGUI), 60 (HUD) | 0..your screen's refresh rate | How many times per second the screen is drawn. 0 means as often as your screen refreshes. |
| SyncGameFps | Toggle | true | | Only in ClickGUI. While a client screen is open, the game runs at most as fast as Fps. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/integration/backend/browser/BrowserSettings.kt)*
