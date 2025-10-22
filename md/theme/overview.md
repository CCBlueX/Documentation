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

The LiquidBounce theme is included in LiquidBounce. However, if you want to create your own theme, see the "Creating Your Own Theme" section below.

### Installing Themes from Marketplace

The easiest way to install themes is through the built-in Marketplace:

1. **Browse available themes**: `.marketplace list theme`
   - This displays all themes available in the marketplace

2. **Install a theme**: Click on your desired theme, which will run:
   - `.marketplace install <id>`
   - The theme will be automatically downloaded and installed

3. **Apply the theme**: After installation, use:
   - `.client theme list` to see all installed themes
   - Click on the theme you just installed, which will run `.client theme set <id>`

### Themes

#### JelloBounce Theme
![JelloBounce HUD](/images/theme/jellobounce/hud.png)
![JelloBounce ClickGUI](/images/theme/jellobounce/clickgui.png)
![JelloBounce Main Menu](/images/theme/jellobounce/mainmenu.png)

Install with: `.marketplace install 265`  
[Repository](https://github.com/CCBlueX/LiquidBounce-Theme-JelloBounce)

#### BeautifyV2 Theme
![BeautifyV2 HUD](/images/theme/beautifyv2/ingame-hud.png)
![BeautifyV2 ClickGUI](/images/theme/beautifyv2/ingame-clickgui.png)

Install with: `.marketplace install 581`  
[Repository](https://github.com/CCBlueX/LiquidBounce-Theme-BeautifyV2)

#### Wurst Theme
![Wurst HUD](/images/theme/wurst/ingame-hud.png)
![Wurst ClickGUI](/images/theme/wurst/clickgui.png)
![Wurst Main Menu](/images/theme/wurst/title.png)

Install with: `.marketplace install 561`  
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