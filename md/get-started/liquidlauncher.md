## Using LiquidLauncher

LiquidLauncher is our custom Minecraft launcher for LiquidBounce. It installs the client, keeps it up to date and starts it. To download it, sign in and start the game for the first time, follow [Installation](/docs/get-started/installation).

On Arch Linux, install `liquidlauncher-bin` or `liquidlauncher-appimage` from the AUR. On NixOS, run `nix run github:CCBlueX/LiquidLauncher`. On macOS, see [LiquidLauncher On MacOS](/docs/get-started/liquidlauncher-on-macos).

![liquidlauncher](/images/liquidlauncher-main.png)

*Launch LiquidBounce* starts the build shown on the left, with its changelog and the Minecraft versions it supports. The cog next to your account opens the settings.

While the game runs, *Log* shows the client log. *Upload log* gives you a link to share when you ask for support.

![log](/images/liquidlauncher-log.png)

### Signing in

![login](/images/liquidlauncher-login.png)

*Microsoft login* opens the Microsoft sign-in. *Microsoft device login* gives you a code to enter at [microsoft.com/link](https://microsoft.com/link) on any device. An offline account only needs a name of 1 to 16 letters, numbers or underscores and cannot join servers that verify accounts.

## Settings

### General

![general](/images/liquidlauncher-general.png)

- *JVM Distribution*: *Automatic* picks a Java for the Minecraft version, *Manual* lets you choose Temurin, GraalVM or Zulu and *Custom* uses a Java you installed yourself
- *Memory*: how much RAM the game may use, see [Fixing FPS](/docs/troubleshooting/fixing-fps)
- *Keep launcher running*: keeps the launcher open while the game runs

*Clear Data* deletes everything the launcher downloaded, including the game folder.

### Minecraft

Uses worlds, resource packs and shader packs from another Minecraft installation without copying them. Pick its directory or leave it on *Auto-detect* and enable what you want to link.

### Client

![client](/images/liquidlauncher-client.png)

*Build* is the LiquidBounce version that starts. Open it to pick an older one, or enable *Show nightly builds* to also list pre-releases. Nightly builds have the latest changes but are not tested yet, so most players should stay on releases.

![mods](/images/liquidlauncher-mods.png)

Mods marked *Recommended* are tested with LiquidBounce and mostly improve performance. Leave them as they are unless one causes trouble. *Add file* installs a mod from your computer and *Browse* searches [Modrinth](https://modrinth.com/). Mods from Modrinth show *Update* once a newer version is out. Mods are kept per Minecraft version, so make sure each one fits the version you play. Our [video](https://www.youtube.com/watch?v=hJEouT54I2M) shows the whole process.

Below the mods, *Browse* next to *Add-ons*, *Themes* and *Scripts* searches the Marketplace. Open an item to see its screenshots and versions, then press *Install*. *Remove* takes it out again.

![browse](/images/liquidlauncher-browse.png)

![add-on](/images/liquidlauncher-addon.png)

The `.marketplace` [commands](/docs/commands/marketplace) in game manage the same items, see [Add-ons](/docs/add-on-api/using-add-ons) for what they do.

### Premium

Donators sign in with their LiquidBounce account here to skip the advertisements, see [Launcher Setup](/docs/premium/launcher-setup). The launcher shares this account with the client, so signing in to either one signs in both.
