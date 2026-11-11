## GuiRenderer

Controls the built-in browser that draws LiquidBounce's menus, like the ClickGUI and the HUD.

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Quality | Decimal | 1.0 | 0.5..1.0 | How sharp the menus are drawn. 1.0 is full sharpness. Lower it if the menus make your game slow. |
| Backend | Choice | Ask | Ask, Chromium, plus any browser an add-on brings | Which browser draws the menus. On Ask, the client lets you pick one when it starts. A change works after you restart the game. |
| AcceleratedPaint | Choice | Auto | Auto, On, Off | Lets your graphics card hand the menus straight to the game, which is faster. Auto only turns it on where it is known to work. Only there while the Chromium add-on is installed. |

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/613dfacc9/src/main/kotlin/net/ccbluex/liquidbounce/integration/backend/browser/BrowserSettings.kt)*
