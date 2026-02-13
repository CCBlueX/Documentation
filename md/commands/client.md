## Client Commands

Client commands manage core client features such as modules, bindings, friends, configurations, and client settings.

---

### `.toggle`

Enable or disable a module.

**Aliases:** `t`

**Usage:**
```
.toggle <module>
```

**Parameters:**
- `module` (required) — The name of the module to toggle.

**Example:**
```
.toggle KillAura
.t Speed
```

---

### `.bind`

Bind a module to a keyboard key.

**Usage:**
```
.bind <module> <key> [action] [modifiers...]
```

**Parameters:**
- `module` (required) — The module to bind.
- `key` (required) — The key name. Common formats: `r`, `y`, `left.control`, `right.alt`, `keypad.4`, `mouse4`. Use `none` to unbind.
- `action` (optional) — The bind action: `Toggle` (default) or `Hold`.
- `modifiers` (optional, vararg) — Modifier keys: `Alt`, `Control`, `Shift`, `Super`.

**Example:**
```
.bind KillAura left.control
.bind fly right.alt Toggle
.bind fly y
.bind fly y Hold
.bind fly y Toggle
.bind fly keypad.4
```

---

### `.binds`

Manage all module key bindings.

**Subcommands:**
- `.binds add <module> <key> [action] [modifiers...]` — Add a new binding.
- `.binds remove <module> <key>` — Remove a binding.
- `.binds list` — List all current bindings.
- `.binds clear` — Remove all bindings.

---

### `.help`

Display a paginated list of all available commands with their aliases and descriptions.

**Usage:**
```
.help [page]
```

**Parameters:**
- `page` (optional) — The page number to display.

---

### `.friend`

Manage your friend list. Friends can be excluded from combat targeting.

**Subcommands:**
- `.friend add <name> [alias]` — Add a player to your friend list with an optional display alias.
- `.friend remove <name>` — Remove a player from your friend list.
- `.friend alias <name> <alias>` — Set a display alias for a friend.
- `.friend list` — List all friends.
- `.friend clear` — Remove all friends.

**Example:**
```
.friend add Steve
.friend add Steve
.friend add SenkJu "Senk Ju"
.friend remove Steve
```

> **Note:** Use double quotes around arguments that contain spaces, for example `.friend add SenkJu "Senk Ju"`.

> Minecraft usernames cannot contain spaces — `.friend add "Senk Ju"` is not a valid username. Quotes are useful for aliases or display names when the command supports them.

---

### `.hide`

Hide or unhide modules from the GUI array list.

**Subcommands:**
- `.hide hide <module>` — Hide a module.
- `.hide unhide <module>` — Unhide a module.
- `.hide list` — List all hidden modules.
- `.hide clear` — Unhide all modules.

---

### `.panic`

Quickly disable all active modules or all modules in a specific category.

**Usage:**
```
.panic [category]
```

**Parameters:**
- `category` (optional) — `all` (default), `nonrender`, or a specific category name (e.g. `combat`, `movement`).

**Example:**
```
.panic
.panic nonrender
.panic combat
```

---

### `.clear`

Clears the in-game chat history.

**Usage:**
```
.clear
```

---

### `.value`

Get or set module settings (values).

**Subcommands:**
- `.value set <path> <value>` — Set a setting to a new value.
- `.value reset <path>` — Reset a single setting to its default.
- `.value reset-all <path>` — Reset all settings in a value group to their defaults.

**Parameters:**
- `path` — The dot-separated path to the setting (for example: `modules.killaura.range`, `modules.aspect.ratio`, or `settings.commands.prefix`). The path can reference module values, global settings, or other configuration paths.
- `value` — The new value to set.

**Example:**
```
.value set modules.killaura.range 4.5
.value set modules.aspect.ratio 2
.value set settings.commands.prefix !
.value reset modules.killaura.range
.value reset-all modules.killaura
```

---

### `.config`

Load and manage online configurations.

**Subcommands:**
- `.config load <name> [modules...]` — Load a configuration by name. Optionally specify which modules to load.
- `.config list` — List available online configurations.
- `.config browse` — Open the configuration browser.
- `.config reload` — Reload configurations from the server.

---

### `.localconfig`

Save, load, and manage local configuration files.

**Subcommands:**
- `.localconfig save <name>` — Save the current configuration to a local file.
- `.localconfig load <name> [modules...]` — Load a local configuration. Optionally specify which modules to load.
- `.localconfig list` — List all local configurations.
- `.localconfig browse` — Open the local config folder.

---

### `.targets`

Toggle target types for combat and visual modules.

**Aliases:** `target`, `enemies`, `enemy`

**Subcommands:**
- `.targets combat <target>` — Toggle a target type for combat modules.
- `.targets visual <target>` — Toggle a target type for visual modules.

**Target options:** `Players`, `Hostile`, `Angerable`, `WaterCreature`, `Passive`, `Invisible`, `Dead`, `Sleeping`, `Friends`, `Self` (visual only).

**Example:**
```
.targets combat Players
.targets visual Invisible
```

---

### `.script`

Manage client scripts.

**Subcommands:**
- `.script reload` — Reload all scripts.
- `.script load <name>` — Load a script by name.
- `.script unload <name>` — Unload a script.
- `.script debug <name>` — Start debug protocol for a script.
- `.script list` — List all loaded scripts.
- `.script browse` — Open the scripts folder.
- `.script edit <name>` — Open a script for editing.

---

### `.debug`

Collect debug information about the client and upload it to a paste service.

**Usage:**
```
.debug
```

Generates a report containing client version, Minecraft version, Java version, OS, profile info, active modules, and loaded scripts.

---

### `.client`

Manage core client settings and features.

**Subcommands:**

| Subcommand | Description |
|---|---|
| `.client info` | Display client name, version, and author |
| `.client prefix <prefix>` | Change the command prefix |
| `.client language list` | List available languages |
| `.client language set <code>` | Set the client language |
| `.client language unset` | Reset to the default language |
| `.client theme list` | List available themes |
| `.client theme set <name>` | Apply a theme |
| `.client theme browse` | Open the themes folder |
| `.client theme reload` | Reload themes |
| `.client appearance hide` | Hide the client overlay |
| `.client appearance show` | Show the client overlay |
| `.client browser open <url>` | Open a URL in the built-in browser |
| `.client integration menu` | Show the integration menu URL |
| `.client integration url` | Show the integration URL |
| `.client integration reset` | Reset the integration URL |
| `.client account login` | Log in to your LiquidBounce account via OAuth |
| `.client account logout` | Log out of your LiquidBounce account |
| `.client account info` | Display account information |
| `.client cosmetics refresh` | Refresh cosmetics from the server |
| `.client cosmetics manage` | Open the cosmetics management page |
| `.client config backup` | Backup all configurations |
| `.client config restore` | Restore configurations from backup |
| `.client config reset` | Reset all configurations to defaults |
| `.client config browse` | Open the configuration folder |
| `.client destruct [confirm] [wipe]` | Remove client traces (use with caution) |

---

### `.chat`

Send a message to LiquidChat (built-in IRC).

**Usage:**
```
.chat <message>
```

> **Note:** Requires the ClientChat global setting to be enabled and connected.

---

### `.chatjwt`

Request a new JWT authentication token from the LiquidChat server.

**Usage:**
```
.chatjwt
```
