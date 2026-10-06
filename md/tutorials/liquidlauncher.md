## Using LiquidLauncher

We recommend using LiquidLauncher to install LiquidBounce. It is a custom Minecraft launcher we designed specifically to make installing and updating our client as straightforward as possible. Simply download the version for your OS from the [downloads](/download) page on our website and install it. After the installation, you should find a new shortcut on your desktop (on Windows only) and in your start menu. Run it and sign in either with your Microsoft account or an offline account to get started.

On Arch Linux, install `liquidlauncher-bin` or `liquidlauncher-appimage` from the AUR. On NixOS, run `nix run github:CCBlueX/LiquidLauncher`.

![liquidlauncher](/images/liquidlauncher-main.png)

The home screen shows the build that will start, its changelog and the Minecraft versions it supports. While the game runs, *Log* shows the client log, which you can upload when asking for support, and *Terminate* stops the game. The cog next to your account opens the settings.

![log](/images/liquidlauncher-log.png)

### Signing in

![login](/images/liquidlauncher-login.png)

Besides the normal Microsoft login there is a device login, which gives you a code to enter in your browser. An offline account only needs a name of 1 to 16 letters, numbers or underscores and cannot join servers that verify accounts. The launcher shares the LiquidBounce account with the client, so signing in to either one signs in both.

## Settings

### General

![general](/images/liquidlauncher-general.png)

- *JVM Distribution*: *Automatic* picks a Java for the Minecraft version, *Manual* lets you choose Temurin, GraalVM or Zulu and *Custom* uses a Java you installed yourself
- *Data Location*: where the launcher keeps its files
- *Memory*: how much RAM the game may use, see [Fixing FPS](/docs/tutorials/fixing-fps)
- *Concurrent Downloads*: how many files are downloaded at once
- *Keep launcher running*: keeps the launcher open while the game runs

*Sign out of Minecraft Account* removes your account and *Clear Data* deletes the launcher's data.

### Minecraft

Here you can use worlds, resource packs and shader packs from another Minecraft installation without copying them. Select its directory or leave it on *Auto-detect* and enable what you want to link.

### Client

![client](/images/liquidlauncher-versions.png)

The *Client* tab shows the build LiquidBounce starts with and everything installed for it.

#### Selecting a LiquidBounce version

Open the build to select the latest version of LiquidBounce or a specific one. When *Show nightly builds* is enabled, LiquidLauncher will also list pre-release versions. These versions contain the latest changes but have not been thoroughly tested yet and therefore might also contain bugs. We recommend only using nightly builds if you know what you are doing. Most users should stick to regular releases.

#### Managing mods

![mods](/images/liquidlauncher-mods.png)

Mods are listed for the Minecraft version of the selected build. The ones marked *Recommended* are a curated list of mods that have been tested to be compatible with LiquidBounce and might improve your experience with the client. Most of them do not alter the gameplay in any way but improve performance and security. You probably will not have to change any default values here unless you are facing issues with one of them.

LiquidLauncher also allows you to install any additional mod you would like to use. Simply make sure the mod you want to install is compatible with the version of Minecraft and LiquidBounce you are intending to play on. *Add file* installs a mod from your computer and *Browse* searches [Modrinth](https://modrinth.com/), whose mods can be updated here later. Once a mod has been installed, it will be automatically applied when the game is launched. You can also disable a mod or delete it entirely if you do not want to use it anymore. Another popular source for mods is [CurseForge](https://www.curseforge.com/).

Please be aware that additional mods have to be installed for every Minecraft version separately.

We also have a video on our YouTube channel showing you how to install additional mods.

<div class="fluid-width-video-wrapper" style="padding-top: 50%;">
    <iframe class="video js-responsive-video" src="https://www.youtube.com/embed/hJEouT54I2M?si=xcznUiw4QCf6ceeN" style="border:0" allowfullscreen="" id="fitvid0"></iframe>
</div>

#### Add-ons, themes and scripts

Below the mods, *Browse* searches the Marketplace for add-ons, themes and scripts. Open an item to see its screenshots and versions and press *Install*. *Remove* takes it out again and *Undo* brings back an item you just removed.

![browse](/images/liquidlauncher-browse.png)

![add-on](/images/liquidlauncher-addon.png)

The `.marketplace` [commands](/docs/commands/marketplace) in game manage the same items, see [Add-ons](/docs/add-on-api/using-add-ons) for what they do.

### Premium

Donators can sign in with their LiquidBounce account here to skip the advertisements, see [Launcher Setup](/docs/premium/launcher-setup).
