## ClickGUI

ClickGUI is the menu where you find, turn on and set up every module. Press **Right Shift** to open it. You can change the key like any other module bind.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Scale | Decimal | 1.0 | 0.5..2.0 | Size of the menu. |
| SearchBarAutoFocus | Toggle | true | | You can type in the search bar right after opening the menu. |
| Snapping | Toggleable Group | On | | Panels line up on a grid when you drag them. |
| Snapping → GridSize | Integer | 10 px | 1..100 px | Size of the grid. |
| Cache | Toggle | true | | Keeps the menu loaded so it opens faster. |
| Renderer | Setting Group | | | See [Shared: Renderer](/docs/modules/shared-settings/renderer). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleClickGui.kt)*
