## Theme System
LiquidBounce features a Theme System that allows you to customize the appearance of the client. The theme affects all graphical user interfaces (GUIs) throughout the client, including but not limited to the HUD, ClickGUI, main menu, and any other visual elements.

<div class="fluid-width-video-wrapper" style="padding-top: 50%;">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/hUZBVYX9jTM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

### LiquidBounce Theme
The default theme of LiquidBounce provides a clean and modern look:

![Default HUD](/images/theme/liquidbounce/hud.png)
![Default ClickGUI](/images/theme/liquidbounce/clickgui.png)
![Default Main Menu](/images/theme/liquidbounce/mainmenu.png)

The LiquidBounce theme is included in LiquidBounce. However, if you want to create your own theme, see the [Creating Your Own Theme](#creating-your-own-theme) section below.

### Installing Themes from Marketplace

The easiest way to install themes is through the built-in Marketplace:

1. **Browse available themes**: `.marketplace list theme`
   - This displays all themes available in the marketplace

2. **Install a theme**: Click on your desired theme, which will run:
   - `.marketplace subscribe <id>`
   - The theme will be automatically downloaded and installed

3. **Apply the theme**: After installation, use:
   - `.client theme list` to see all installed themes
   - Click on the theme you just installed, which will run `.client theme set <id>`

### Themes

#### JelloBounce Theme
![JelloBounce HUD](/images/theme/jellobounce/hud.png)
![JelloBounce ClickGUI](/images/theme/jellobounce/clickgui.png)
![JelloBounce Main Menu](/images/theme/jellobounce/mainmenu.png)

Install with: `.marketplace subscribe 265`  
[Repository](https://github.com/CCBlueX/LiquidBounce-Theme-JelloBounce)

#### BeautifyV2 Theme
![BeautifyV2 HUD](/images/theme/beautifyv2/ingame-hud.png)
![BeautifyV2 ClickGUI](/images/theme/beautifyv2/ingame-clickgui.png)

Install with: `.marketplace subscribe 581`  
[Repository](https://github.com/CCBlueX/LiquidBounce-Theme-BeautifyV2)

#### Wurst Theme
![Wurst HUD](/images/theme/wurst/ingame-hud.png)
![Wurst ClickGUI](/images/theme/wurst/clickgui.png)
![Wurst Main Menu](/images/theme/wurst/title.png)

Install with: `.marketplace subscribe 561`  
[Repository](https://github.com/CCBlueX/LiquidBounce-Theme-Wurst)

### Creating Your Own Theme

For developers who want to create custom themes:

1. **Clone the theme template**:
   ```bash
   git clone https://github.com/CCBlueX/LiquidBounce-Theme
   cd LiquidBounce-Theme
   ```

2. **Edit the metadata file** (`public/metadata.json`):
   ```json
   {
     "id": "your-custom-id",
     "name": "YourTheme",
     "version": "0.1.0",
     "authors": ["YourName"]
   }
   ```
   Change from the default:
   ```json
   {
     "id": "liquidbounce",
     "name": "LiquidBounce",
     "version": "0.1.0",
     "authors": ["CCBlueX"]
   }
   ```
   The optional `nativeFont` field names one of the theme's loaded font faces (for example `"nativeFont": "Inter Medium"`) that the client draws its own text with. If your theme does not set it, the client uses the font of the included LiquidBounce theme, or a system font if that is unavailable.

   The optional `sounds` field lists the names of sounds your theme ships as `public/sounds/<name>.ogg` (for example `"sounds": ["click"]`). Names must be valid Minecraft identifier paths without `/`. The client registers each sound with the game's sound engine as `liquidbounce:theme/<theme id>/<name>`. Your theme can play any registered sound, including its own, by sending a `POST` request to `/api/v1/client/sound` with a JSON body such as `{"sound": "liquidbounce:theme/your-custom-id/click", "volume": 1.0, "pitch": 1.0}`. `volume` and `pitch` are optional and default to `1.0`. Sounds play in the UI category, so the game's volume sliders apply.

   The optional `splash` field gives your theme its own loading screen: a [Lottie](https://airbnb.io/lottie/) animation the client draws itself, with background, text and accent colors. See [Splash Screen](/docs/theme-system/splash-screen) for the format and its limits.

3. **Install dependencies and start development server**:
   ```bash
   npm install
   npm run dev
   ```

4. **Test your theme in LiquidBounce**:
   - In the game chat, type: `.client theme set http://localhost:5173/`
   - Your theme will load in real-time as you make changes

5. **Publish to Marketplace**:
   - Once your theme is ready, you can submit it to the Marketplace for others to use by [contacting us](https://ccbluex.net/contact).

### Security Warning

> **Only install themes from trusted sources!**
>
> Themes can establish HTTP/WebSocket connections to external servers, which means malicious themes could:
> - Take over control of your client
> - Steal sensitive information
> - Perform unauthorized actions
>
> We strongly discourage downloading themes from unknown sources or untrusted developers. Always use the official Marketplace when possible.