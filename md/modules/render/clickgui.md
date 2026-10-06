## ClickGUI

ClickGUI opens the main menu where you browse, toggle, and configure every module in LiquidBounce. By default it's bound to **Right Shift** — press it in-game to bring up the interface, search for what you need, and tweak settings without leaving your session. This is the central hub from which you'll manage everything from [KillAura](/docs/modules/combat/killaura) to [ESP](/docs/modules/render/esp).

You can resize the whole interface to fit your screen, have the search bar grab focus automatically when the menu opens, and snap module panels neatly to a grid as you drag them around. The menu is always available regardless of whether you're connected to a server, so it's the first thing you'll reach for when setting up your client.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Scale | Decimal | 1.0 | 0.5..2.0 | Adjusts the overall size of the menu. Lower values shrink everything to fit more on screen; higher values make panels and text larger and easier to read. |
| SearchBarAutoFocus | Toggle | true | — | When on, the search bar is focused the moment you open the menu, so you can start typing a module name right away without clicking it first. |
| Snapping | Toggleable Group | on | — | When enabled, panels snap to an invisible grid as you move them, keeping your layout aligned and tidy. |
| Snapping → GridSize | Integer | 10 px | 1..100 | The spacing of the snapping grid in pixels. Smaller values allow finer positioning; larger values snap panels to wider intervals. |
| Cache | Toggle | true | — | Keeps the menu loaded in the background so it reopens instantly and remembers its state. Turning this off frees resources but the menu may take longer to appear. |
| Renderer | Setting Group | — | — | See [Shared: Renderer](/docs/modules/shared-settings/renderer). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleClickGui.kt)*
