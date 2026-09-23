## Configs

Configs are shared on the LiquidBounce marketplace. Anyone with a LiquidBounce account can publish one, and everyone can load them in game. Configs picked by the LiquidBounce team are featured and always listed first.

Everything runs through the `.config` command. Type `.config ` and the chat suggests its subcommands.

![Config subcommands](/images/configs/suggestions.png)

### Finding a Config

`.config list [page]` lists ten configs per page: featured ones first, then the rest ranked by recent reports, downloads and age.

![Config list](/images/configs/list.png)

Each entry shows:

- **`author/name`**: click it to put `.config load author/name` into the chat
- **`[✔ 4] [✘ 0]`**: how many players reported in the last 30 days that the config works or is broken. Click either one to add your own report
- **The servers it was made for**
- **The Minecraft version it was made on**, green when it matches the version you are playing on and red when it does not
- **Its tags and when it was last updated**. Hover the date to see the exact day

`.config search <query> [tag]` searches config names. Add a tag to only search within it; the chat suggests the available tags.

![Search](/images/configs/search.png)

![Search within a tag](/images/configs/search-tag.png)

`.config info <config>` shows one config in full, including the servers, tags and everything it needs to load.

![Config info](/images/configs/info.png)

![Config with dependencies](/images/configs/info-dependencies.png)

#### Naming a Config

Every command that takes a config accepts:

- `author/name`, such as `CCBlueX/hypixel`
- the name alone, such as `hypixel`, as long as only one author uses it
- the numeric ID
- a share code, such as `LB-FLNV95DU`

When several authors use the same name, the command lists them and asks you to pick one.

![Ambiguous name](/images/configs/ambiguous.png)

### Loading a Config

`.config load <config>` applies a config. Add a comma-separated list of modules, such as `.config load CCBlueX/grim KillAura,Velocity`, to only take those modules from it. A link to a config file works as well.

![Loading a config](/images/configs/load.png)

![Loading only some modules](/images/configs/load-modules.png)

If the config was made for a different Minecraft version, LiquidBounce tells you and asks you to reconnect with the right one. See [Changing Version](/docs/usage/changing-version).

![Config for another version](/images/configs/load-code.png)

#### Dependencies

A config can depend on other configs, add-ons and scripts. Loading it first loads the configs it depends on, in order, and then applies its own settings on top. Add-ons and scripts it needs are installed, including whatever they need themselves. Restart the game to finish installing them.

![Loading a config with dependencies](/images/configs/load-dependencies.png)

#### Changing a Loaded Config

LiquidBounce remembers which config you loaded. As soon as you change one of its settings, `.config info` marks it as edited.

![Edited config](/images/configs/info-edited.png)

- `.config revert` drops your changes and goes back to the config as published
- `.config restore` brings back the settings you had before you loaded your first marketplace config
- `.config detach` stops tracking the config and keeps your settings as they are

![Revert](/images/configs/revert.png)

![Restore](/images/configs/restore.png)

![Detach](/images/configs/detach.png)

### Reporting

`.config report works [config]` and `.config report broken [config]` tell others whether a config works for you. Without a config, the report is for the one you loaded. Clicking `[✔]` or `[✘]` in a list does the same. Reports count for 30 days and decide how high a config ranks.

![Reporting](/images/configs/report.png)

### Auto Config

The [AutoConfig](/docs/modules/misc/autoconfig) module loads the best config for a server when you join it. Its tag in the array list shows which config is loaded, followed by `*` once you changed something.

![AutoConfig](/images/configs/autoconfig.png)

![AutoConfig after a change](/images/configs/autoconfig-edited.png)

By default it only loads featured configs. Turn off **OnlyFeatured** to also load configs published by other players.

![AutoConfig settings](/images/configs/clickgui.png)

### Publishing a Config

Log in to your LiquidBounce account with `.client account login` first.

A published config holds your module settings. It leaves out your binds, which modules you hid from the array list, and the settings of Render and Fun modules.

#### New Config

`.config publish new <name> [public|unlisted] [description]` publishes your current settings. When you are on a server, it becomes the server the config is made for. Each of your configs needs its own name.

![Publishing a config](/images/configs/publish-new.png)

#### Overlay

An overlay only holds what you changed. Load a config, change what you want and run `.config publish overlay <name> [public|unlisted] [description]`. The overlay depends on the config you loaded, so loading it loads that config first. When its author updates it, your overlay keeps building on the new version.

![Publishing an overlay](/images/configs/publish-overlay.png)

#### Fork

A fork is a full copy of someone else's config with your changes, and its info links back to the original. Load it, change what you want and run `.config publish fork <name> [public|unlisted] [description]`.

![Publishing a fork](/images/configs/publish-fork.png)

#### Public and Unlisted

A public config shows up in lists and searches. An unlisted one does not, so hand out its share code instead: `.config load LB-...` loads it. The share code is shown when you publish an unlisted config, and `.config info` shows it to you as the author.

![Share code in the config info](/images/configs/info-own.png)

### Managing Your Configs

The `.config edit` commands change the config you loaded, which has to be one of yours.

`.config edit update [changelog]` publishes your changes as a new version. For an overlay, the update again only holds the modules that differ from the config it builds on.

![Updating a config](/images/configs/edit-update.png)

`.config edit set` changes the details:

| Command | Changes |
|---|---|
| `.config edit set name <name>` | The name |
| `.config edit set description <text>` | The description |
| `.config edit set tags <tag>, <tag>` | The tags. Leave it empty to remove them all |
| `.config edit set servers <server> <server>` | The servers it is made for. Leave it empty to remove them all |
| `.config edit set visibility <visibility>` | `public` or `unlisted` |

![Setting servers and tags](/images/configs/edit-set.png)

![Making a config public](/images/configs/edit-visibility.png)

`.config edit depend add <item>` adds a config, add-on or script your config needs, and `.config edit depend remove <item>` removes it again. Configs it depends on load in the order you added them.

![Adding a dependency](/images/configs/edit-depend.png)

`.config edit delete` deletes the config.

![Deleting a config](/images/configs/delete.png)
