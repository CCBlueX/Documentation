## Add-ons

Add-ons extend LiquidBounce with features that are compiled into a jar file instead of being written in JavaScript. An add-on can register its own modules, commands and HUD components, and even its own module categories, which appear in the [ClickGUI](/docs/usage/clickgui) next to the built-in ones. For smaller features, [scripts](/docs/Script%20API/Installation) remain the simpler option. They run on the Script API, which is an add-on itself.

### Installing Add-ons

Add-ons are distributed through the built-in Marketplace:

1. **Browse available add-ons**: `.marketplace list addon`
   - This displays all add-ons available in the marketplace, each with its ID

   ![Marketplace Add-ons](/images/addons/marketplace-list.png)

2. **Install an add-on**: `.marketplace subscribe <id>`
   - The add-on is downloaded and prepared for the next start

   ![Subscribing to an Add-on](/images/addons/marketplace-subscribe.png)

3. **Restart the client**
   - Add-ons are loaded while LiquidBounce starts up, so a newly installed or updated add-on becomes active after you restart the game
   - `.addon list` then shows it, and `.addon info <name>` shows what it registered

   ![Installed Add-ons](/images/addons/addon-list.png)

   ![Add-on Info](/images/addons/addon-info.png)

Use `.marketplace unsubscribe <id>` to remove an add-on again and `.marketplace update` to pull the latest revision of everything you are subscribed to.

Every revision of an add-on is built for a certain Minecraft and LiquidBounce version, so only the revisions that fit the game you are running are installed. An add-on whose revisions all miss your version stays subscribed without being installed and returns once a revision that fits is available.

Modules of an add-on appear in the ClickGUI under the category it registers:

![Extras in the ClickGUI](/images/addons/clickgui-extras.png)

#### Official Add-ons

- **[Extras](https://github.com/CCBlueX/LiquidBounce-Addon-Extras)**: modules LiquidBounce does not ship. Install with: `.marketplace subscribe 781`
- **[Script API](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI)**: runs [scripts](/docs/script-api/installation). Install with: `.marketplace subscribe 771`

> Add-ons run with the same permissions as the client itself. Only install add-ons from the official Marketplace or from developers you trust.

### Developing Add-ons

Start from the [add-on template](https://github.com/CCBlueX/LiquidBounce-Addon-Template). LiquidBounce itself is published as a Maven artifact, so an add-on can be compiled against it. Release builds are served from `https://maven.ccbluex.net/releases`, development builds from `https://maven.ccbluex.net/snapshots`. Both are published together with a sources artifact.

Add-ons can be written in Java as well as Kotlin. The classes an add-on builds on expose Java-friendly signatures — event listeners, for instance, are registered through `on`, `onTick`, `every` and `after`, which take plain `Consumer` and `Runnable` callbacks and return an `AutoCloseable` that unregisters the listener again. This public surface is tracked in an API dump in the LiquidBounce repository, so changes that would break add-ons are caught before they are released.

A module category registered by an add-on can bring its own icon for the ClickGUI. The icon is an SVG or PNG bundled in the add-on's jar and is passed to the category as an identifier in the form `namespace:path`, which resolves to `resources/<namespace>/<path>` inside the jar. Place the file there rather than in Minecraft's `assets/`, since anything that inspects the loaded resource packs can see those. Categories without an icon fall back to the icon the theme provides, as the built-in categories do.

An add-on can also draw onto the HUD. A component it registers behaves like the components a theme ships: it is listed in the [HUD Editor](/docs/theme-system/hud-customization), can be moved and anchored freely and shows its settings there. A component can either be registered directly, in which case it is part of the HUD right away, or through a factory, which puts it into the **Add Component** drawer under the name and description the factory carries so players add it themselves. The position and settings of such a component are not written to the config; the add-on keeps that state.

An add-on can also provide its own browser backend, which is what the client renders its web-based interfaces with. The add-on registers the backend under an id, a name and a description, and unless the backend is marked as not selectable, it is offered next to the built-in ones in a selection screen shown while LiquidBounce starts up. The backend chosen there is stored in the config, so the choice only has to be made once.

### Publishing Add-ons

The template's build workflow uploads your add-on to the Marketplace whenever you publish a GitHub release.

1. **Create the add-on**: open **Resources** from the account menu on [liquidbounce.net](https://liquidbounce.net/account/resources) and fill in **New add-on**
   - It then appears under **Your resources** with its ID

   ![New Add-on](/images/addons/new-addon.png)

   ![Your Resources](/images/addons/resources.png)

2. **Generate an API token** on the same page
   - The token is shown only once. Regenerating it stops the old one from working

   ![API Token](/images/addons/api-token.png)

3. **Connect your repository**: under **Settings > Secrets and variables > Actions**, add

   | Kind | Name | Value |
   |---|---|---|
   | Variable | `MARKETPLACE_ITEM_ID` | The ID of your add-on |
   | Secret | `API_TOKEN` | Your API token |

4. **Publish a release**
   - The tag becomes the version and the release notes become the changelog. Pre-releases are skipped

An upload is a zip holding exactly one jar, which the template's workflow builds for you. Uploads wait for a review by the LiquidBounce team before players receive them, unless your account is a trusted publisher.
