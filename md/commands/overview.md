## Commands Overview

Commands are short messages you type into the Minecraft chat to control LiquidBounce. Every command starts with the prefix, which is a dot (`.`) unless you changed it.

The commands are split into these pages:

- [Client](/docs/commands/client): modules, key binds, friends, configs and client settings.
- [In-Game](/docs/commands/in-game): your position, ping, the server, teleporting and walking.
- [Creative](/docs/commands/creative): give, rename and enchant items in Creative mode.
- [Module](/docs/commands/module): extra controls for a few modules, like XRay and AutoDisable.
- [Translate](/docs/commands/translate): translate chat text into another language.
- [Marketplace](/docs/commands/marketplace): find and install themes, add-ons and scripts.

### Quick reference

| Command | What it does |
|---|---|
| `.help` | Lists all commands |
| `.toggle <module>` | Turns a module on or off |
| `.bind <module> <key>` | Puts a module on a key |
| `.friend add <name>` | Adds a player to your friends |
| `.config load <config>` | Loads a config from the marketplace |
| `.panic` | Turns off every module except Render modules |
| `.client prefix <prefix>` | Changes the command prefix |
| `.ping` | Shows your ping |
| `.coordinates info` | Shows where you are |

### How to type commands

Open the chat and start your message with the prefix. Words in `<angle brackets>` must be filled in. Words in `[square brackets]` are optional and can be left out. Press Tab while typing to see suggestions.

```
.toggle KillAura
.bind Speed left.alt
.friend add SenkJu
.friend add SenkJu Senk
.value set modules.killaura.range 4.5
.value set settings.commands.prefix !
```

If a value has spaces in it, put it in double quotes, for example `.config load "Author/My Config"`.

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/command/CommandManager.kt)*
