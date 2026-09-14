## Add-ons

Add-ons extend LiquidBounce with additional features and are compiled into a jar file. An add-on can register its own modules and commands, and even its own module categories, which appear in the [ClickGUI](/docs/usage/clickgui) next to the built-in ones.

### Installing Add-ons

Add-ons are distributed through the built-in Marketplace:

1. **Browse available add-ons**: `.marketplace list addon`
   - This displays all add-ons available in the marketplace

2. **Install an add-on**: `.marketplace subscribe <id>`
   - The add-on is downloaded and prepared for the next start

3. **Restart the client**
   - Add-ons are loaded while LiquidBounce starts up, so a newly installed or updated add-on becomes active after you restart the game

Use `.marketplace unsubscribe <id>` to remove an add-on again and `.marketplace update` to pull the latest revision of everything you are subscribed to.

> Add-ons run with the same permissions as the client itself. Only install add-ons from the official Marketplace or from developers you trust.

### Developing Add-ons

LiquidBounce itself is published as a Maven artifact, so an add-on can be compiled against it. Release builds are served from `https://maven.ccbluex.net/releases`, development builds from `https://maven.ccbluex.net/snapshots`. Both are published together with a sources artifact.

Once your add-on is ready, you can submit it to the Marketplace for others to use by [contacting us](https://ccbluex.net/contact).
