## Using Add-ons

Add-ons extend LiquidBounce with features that are compiled into a jar file instead of being written in JavaScript. An add-on can register its own modules, commands and HUD components, and even its own module categories, which appear in the [ClickGUI](/docs/usage/clickgui) next to the built-in ones:

![Extras in the ClickGUI](/images/addons/clickgui-extras.png)

For smaller features, [scripts](/docs/script-api/installation) remain the simpler option. They run on the Script API, which is an add-on itself.

> Add-ons run with the same permissions as the client itself. Only install add-ons from the Marketplace or from developers you trust.

### Installing Add-ons

In [LiquidLauncher](/docs/get-started/liquidlauncher#client), open the **Client** tab in the settings, click **Browse** next to **Add-ons** and install one. The launcher sets the add-on up for the next start, together with the add-ons and scripts it needs.

In game, the chat does the same:

1. **Browse available add-ons**: `.marketplace list addon`

   ![Marketplace Add-ons](/images/addons/marketplace-list.png)

2. **Install an add-on**: `.marketplace subscribe <add-on>`
   - Name the add-on as `author/name`, by its name or by its ID. The chat suggests popular add-ons
   - The add-on is downloaded and prepared for the next start, together with the add-ons and scripts it needs

   ![Subscribing to an Add-on](/images/addons/marketplace-subscribe.png)

3. **Restart the client**
   - Add-ons are loaded while LiquidBounce starts up, so a newly installed or updated add-on becomes active after you restart the game
   - `.addon list` then shows it, and `.addon info <name>` shows what it registered

   ![Installed Add-ons](/images/addons/addon-list.png)

   ![Add-on Info](/images/addons/addon-info.png)

### Updating and Removing

Installed add-ons are updated every time the client starts. `.marketplace update` updates them right away, the update is active after the next restart. `.marketplace unsubscribe <add-on>` removes an add-on; the chat suggests the ones you have installed.

Every revision of an add-on is built for a certain Minecraft and LiquidBounce version, so only the revisions that fit the game you are running are installed. An add-on whose revisions all miss your version stays subscribed without being installed and returns once a revision that fits is available.

### Official Add-ons

- **[Extras](https://github.com/CCBlueX/LiquidBounce-Addon-Extras)**: modules LiquidBounce does not ship. Install with `.marketplace subscribe Extras`
- **[Script API](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI)**: runs [scripts](/docs/script-api/installation). Install with `.marketplace subscribe ScriptAPI`
- **Ultralight**: a lightweight browser for the client's menus. Install with `.marketplace subscribe Ultralight`
- **[Wry](https://github.com/CCBlueX/LiquidBounce-Addon-Wry)**: shows the client's menus with the web view of your system, WebView2 on Windows, WebKit on macOS and WebKitGTK on Linux. Install with `.marketplace subscribe Wry`

### Choosing a Browser

The title screen, the ClickGUI and the HUD are web pages, which LiquidBounce shows with the Chromium browser it comes with. Once an add-on such as Ultralight or Wry offers another browser, the client asks which one to use while it starts:

![Choosing a browser](/images/addons/browser-select.png)

The choice is remembered. To choose again, hold **SHIFT** while the client starts. After the add-on is removed, LiquidBounce goes back to Chromium.

Wry needs the web view of your system. WebView2 comes with Windows 11 and updated Windows 10. On Linux, install WebKitGTK from your distribution, for example `sudo pacman -S webkit2gtk-4.1` or `sudo apt install libwebkit2gtk-4.1-0`.

### Making Your Own

The [Developers](/docs/add-on-api/developers/getting-started) section explains how to write an add-on in Kotlin or Java and publish it on the Marketplace.
