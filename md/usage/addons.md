## Add-ons

Add-ons extend LiquidBounce with features that are compiled into a jar file instead of being written in JavaScript. An add-on can register its own modules, commands and HUD components, and even its own module categories, which appear in the [ClickGUI](/docs/usage/clickgui) next to the built-in ones. For smaller features, [scripts](/docs/Script%20API/Installation) remain the simpler option. They run on the Script API, which is an add-on itself.

### Installing Add-ons

Add-ons are distributed through the built-in Marketplace:

1. **Browse available add-ons**: `.marketplace list addon`
   - This displays all add-ons available in the marketplace, each with its ID

   ![Marketplace Add-ons](/images/addons/marketplace-list.png)

2. **Install an add-on**: `.marketplace subscribe <id>`
   - The add-on is downloaded and prepared for the next start, together with the add-ons and scripts it needs

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

Start from the [add-on template](https://github.com/CCBlueX/LiquidBounce-Addon-Template). The [Add-on API](/docs/add-on-api/getting-started) section covers modules, commands, HUD components, browser backends and the rest, in Kotlin and Java.

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
