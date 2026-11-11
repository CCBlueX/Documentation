## Client Commands

These commands control LiquidBounce itself: modules, key binds, friends, configs and client settings.

Some commands take a list of modules. Separate the names with commas and no spaces, like `KillAura,Speed`.

---

### `.toggle`

Turns a module on or off. Short form: `.t`.

```
.toggle <module>
```

```
.toggle KillAura
.t Speed
```

---

### `.bind`

Puts a module on a key, so pressing the key turns the module on or off.

```
.bind <module> <key> [action] [modifiers...]
```

- `key`: the key name, for example `r`, `y`, `left.control`, `left_shift`, `right.alt`, `keypad.4` or `mouse.4`. Use `none` to remove the bind. If the client does not know the key name, it tells you and binds nothing.
- `action`: `Toggle` turns the module on with one press and off with the next. `Hold` keeps it on only while you hold the key. `Smart` acts like `Hold` when you hold the key and like `Toggle` when you just tap it. If you leave this out, the module keeps the action it had.
- `modifiers`: extra keys that must be held too: `Shift`, `Control`, `Alt` or `Super`. Write them with spaces between, like `Shift Control`.

```
.bind KillAura left.control
.bind Fly y Hold
.bind Fly f Toggle Shift
.bind Fly none
```

---

### `.binds`

Shows and changes the key binds of all modules.

- `.binds add <module> <key> [action] [modifiers]`: binds a module, the same way as `.bind`. Here the modifiers are separated with commas, like `Shift,Control`.
- `.binds remove <modules>`: removes the binds of one or more modules.
- `.binds list [page]`: lists every module that has a bind. Click the red `[✕]` next to one to remove its bind.
- `.binds clear`: removes all binds.

---

### `.help`

Lists all commands with their short forms. Hover over a command to see what it does.

```
.help [page]
```

---

### `.friend`

Keeps a list of your friends. Combat modules leave friends alone unless you turn on `Friends` in the [Targets](/docs/global-settings/targets) settings.

- `.friend add <name> [alias]`: adds a player. The alias is a nickname for them and must be one word.
- `.friend remove <name>`: removes a friend.
- `.friend alias <name> <alias>`: changes a friend's nickname.
- `.friend list`: lists your friends. Click `[X]` to remove one.
- `.friend clear`: removes all friends.

```
.friend add Steve
.friend add SenkJu Senk
.friend remove Steve
```

---

### `.hide`

Hides modules from the module list on your screen. They keep working, you just don't see them in the list.

- `.hide hide <modules>`: hides one or more modules.
- `.hide unhide <modules>`: shows them again.
- `.hide list [page]`: lists hidden modules.
- `.hide clear`: shows all modules again.

```
.hide hide KillAura,Velocity
```

---

### `.panic`

Turns off modules fast.

```
.panic [category]
```

Without a category it turns off every module except Render modules, so your visuals stay. Use `all` to turn off everything, or a category name like `combat` or `movement` to turn off only that category.

```
.panic
.panic all
.panic combat
```

---

### `.clear`

Clears your chat.

```
.clear
```

---

### `.value`

Changes any setting by its path, without opening the ClickGUI. Press Tab while typing a path to see which ones exist.

- `.value set <path> <value>`: sets a setting.
- `.value reset <path>`: puts one setting back to its default.
- `.value reset-all <path>`: puts every setting of a module or group back to its default. Key binds are kept.

Module settings start with `modules.`, global settings with `settings.`.

```
.value set modules.killaura.range 4.5
.value set modules.aspect.ratio 200
.value set settings.commands.prefix !
.value reset modules.killaura.range
.value reset-all modules.killaura
```

---

### `.config`

Finds, loads and shares configs on the marketplace. The [Configs](/docs/usage/configs) guide explains how this works.

| Command | What it does |
|---|---|
| `.config list [page]` | Lists configs on the marketplace |
| `.config search <query> [tag]` | Searches configs, optionally only with one tag |
| `.config info [config]` | Shows a config, or the one you loaded |
| `.config load <config> [modules]` | Loads a config by `author/name`, name, ID, share code or link |
| `.config revert` | Throws away your changes to the loaded config |
| `.config restore` | Brings back the settings you had before your first marketplace config |
| `.config detach` | Stops following the loaded config and keeps your settings |
| `.config report works [config]` | Tells others that a config works for you |
| `.config report broken [config]` | Tells others that a config does not work for you |
| `.config publish new <name> [visibility] [description]` | Shares your current settings |
| `.config publish overlay <name> [visibility] [description]` | Shares only your changes on top of the loaded config |
| `.config publish fork <name> [visibility] [description]` | Shares a copy of someone else's config with your changes |
| `.config edit update [changelog]` | Uploads your changes to your loaded config |
| `.config edit set <field> <value>` | Changes the `name`, `description`, `tags`, `servers` or `visibility` of your loaded config |
| `.config edit depend add <item>` | Adds a config, add-on or script your config needs |
| `.config edit depend remove <item>` | Removes one of those again |
| `.config edit delete` | Deletes your loaded config |

`visibility` is `public` (the default) or `unlisted`. Put names with spaces in double quotes.

---

### `.localconfig`

Saves and loads configs as files on your computer.

- `.localconfig save <name> [overwrite] [include...]`: saves your settings. `.localconfig create` does the same. Add `true` as `overwrite` to replace a file that already exists.
- `.localconfig load <name> [modules]`: loads a saved config. Give module names to load only those modules.
- `.localconfig list [page]`: lists your saved configs. Click one to load it.
- `.localconfig browse`: opens the folder with your configs.

A saved config leaves out your key binds, your hidden modules and the settings of Render and Fun modules, so it does not change someone else's setup. To keep them in the file, list them after the `overwrite` value (`true` or `false`): `binds`, `hidden`, `render` and `fun`.

```
.localconfig save hypixel
.localconfig save hypixel true binds render
.localconfig load hypixel KillAura,Velocity
```

If you were following a marketplace config, loading a whole local config stops that, and the chat tells you which config you left. Loading only some modules, or a file you saved from that marketplace config, keeps it.

---

### `.targets`

Turns a kind of target on or off for combat or visual modules. Short forms: `.target`, `.enemies`, `.enemy`.

- `.targets combat <target>`: for combat modules like KillAura.
- `.targets visual <target>`: for visual modules like ESP.

The targets are `Players`, `Hostile`, `Angerable`, `WaterCreature`, `Passive`, `ArmorStand`, `Invisible`, `Dead`, `Sleeping`, `Friends`, and `Self` (visual only). The [Targets](/docs/global-settings/targets) page explains each one.

```
.targets combat Players
.targets visual Invisible
```

---

### `.liquidchat`

Talks to other LiquidBounce users in LiquidChat. Short form: `.lc`. LiquidChat has to be on in the [Client Chat](/docs/global-settings/client-chat) settings.

- `.liquidchat msg <user> <message>`: sends a private message.
- `.liquidchat report <user> <reason>`: reports a user who breaks the chat rules.

To write to everyone, use `.chat <message>`.

```
.chat Hello everyone!
.lc msg SenkJu Hi there
```

---

### `.addon`

Shows the add-ons you have installed.

- `.addon list`: lists your add-ons and their versions. It also tells you when the game needs a restart to finish installing one.
- `.addon info <name>`: shows an add-on's name, version, authors and how many modules and commands it adds.

---

### `.script`

Manages scripts. This command comes with the [Script API add-on](/docs/script-api/installation).

- `.script list`: lists your scripts.
- `.script load <name>` and `.script unload <name>`: turns a script on or off.
- `.script reload`: reloads all scripts.
- `.script errors <name>`: shows the errors of a script.
- `.script browse`: opens the scripts folder.
- `.script edit <name>`: opens a script in your editor.
- `.script debug <name> [protocol] [suspendOnStart] [inspectInternals] [port]`: starts a script with a debugger attached, for script writers.

---

### `.debug`

Uploads information about your game to [logs.liquidbounce.net](https://logs.liquidbounce.net) and posts the links in chat. Send these links when you ask for help.

```
.debug
```

The upload contains the client, Minecraft, Java and system versions, your account name, the server you are on, your active modules and add-ons, your current settings and the end of your latest game log.

---

### `.client`

Client settings and tools.

| Command | What it does |
|---|---|
| `.client info` | Shows the client name, version and author |
| `.client prefix <prefix>` | Changes the command prefix |
| `.client language list` | Lists the languages the client can use |
| `.client language set <language>` | Sets the client language |
| `.client language unset` | Uses your Minecraft language again |
| `.client theme list [page]` | Lists your themes |
| `.client theme set <theme>` | Switches to a theme |
| `.client theme browse` | Opens the themes folder |
| `.client theme reload` | Loads the themes again |
| `.client browser open <url>` | Opens a website in the built-in browser |
| `.client integration menu` | Shows the links to the client's menus (`.client integration url` does the same) |
| `.client integration reset` | Reloads the client's menus |
| `.client account login` | Logs in to your LiquidBounce account in your web browser |
| `.client account logout` | Logs out of your LiquidBounce account |
| `.client account info` | Shows your LiquidBounce account |
| `.client cosmetics refresh` | Loads cosmetics again |
| `.client cosmetics manage` | Opens the cosmetics page in your web browser |
| `.client config backup [configs]` | Makes a backup of your settings |
| `.client config restore <name>` | Loads a backup |
| `.client config reset [configs]` | Puts your settings back to their defaults |
| `.client config browse` | Opens the backup folder |
| `.client destruct [confirm] [wipe]` | Removes LiquidBounce from the running game |

`.client destruct` asks first. Run `.client destruct yes` to do it, or `.client destruct yes yes` to also delete your LiquidBounce files and game logs.

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/command/commands/client)*
