## Renderer

The Renderer group controls how often the client's custom interfaces are redrawn on screen. Rather than rendering every single game frame, these elements can run on their own framerate, which keeps them smooth while avoiding unnecessary work when nothing on screen is changing.

By default the renderer simply follows your in-game framerate, so the interface looks as fluid as the rest of Minecraft. If you'd prefer to cap how fast these elements refresh — for example to save performance on weaker hardware, or to keep a steady look regardless of your game's FPS — you can turn off the game sync and set your own frame limit.

This setting group is used by the following modules:

- [ClickGUI](/docs/modules/render/clickgui)
- [HUD](/docs/modules/render/hud)

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Fps | Integer | 0 | 0..170 FPS | The framerate the interface renders at. A value of 0 leaves it uncapped. Only takes effect when SyncGameFps is off. |
| SyncGameFps | Toggle | true | — | Matches the interface's refresh rate to your current in-game FPS. Turn this off to use the manual Fps limit instead. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2)*
