## Add-ons

Add-ons extend LiquidBounce with features that are compiled into a jar file instead of being written in JavaScript. An add-on can register its own modules and commands, and even its own module categories, which appear in the [ClickGUI](/docs/usage/clickgui) next to the built-in ones. For smaller features, [scripts](/docs/Script%20API/Installation) remain the simpler option. They run on the Script API, which is an add-on itself.

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

Add-ons can be written in Java as well as Kotlin. The classes an add-on builds on expose Java-friendly signatures — event listeners, for instance, are registered through `on`, `onTick`, `every` and `after`, which take plain `Consumer` and `Runnable` callbacks and return an `AutoCloseable` that unregisters the listener again. This public surface is tracked in an API dump in the LiquidBounce repository, so changes that would break add-ons are caught before they are released.

A module category registered by an add-on can bring its own icon for the ClickGUI. The icon is an SVG or PNG bundled in the add-on's jar and is passed to the category as an identifier in the form `namespace:path`, which resolves to `resources/<namespace>/<path>` inside the jar. Place the file there rather than in Minecraft's `assets/`, since anything that inspects the loaded resource packs can see those. Categories without an icon fall back to the icon the theme provides, as the built-in categories do.

Once your add-on is ready, you can submit it to the Marketplace for others to use by [contacting us](https://ccbluex.net/contact).
