## Commands Overview

LiquidBounce provides a comprehensive set of **commands** that you can type in the Minecraft chat to control the client. All commands begin with the configured prefix (default: `.`).

Commands are organized into the following categories:

- [Client Commands](/docs/Commands/Client%20Commands) — Manage the client, modules, bindings, friends, and configurations.
- [In-Game Commands](/docs/Commands/In-Game%20Commands) — Utilities for in-game information such as coordinates, ping, TPS, and server info.
- [Creative Commands](/docs/Commands/Creative%20Commands) — Item manipulation commands for Creative mode.
- [Module Commands](/docs/Commands/Module%20Commands) — Commands tied to specific modules (XRay, AutoDisable, Teleport, etc.).
- [Translation Commands](/docs/Commands/Translation%20Commands) — Translate text and configure auto-translation.
- [Marketplace Commands](/docs/Commands/Marketplace%20Commands) — Browse and manage marketplace items.

### Quick Reference

| Command | Description |
|---|---|
| `.help` | List all available commands |
| `.toggle <module>` | Enable or disable a module |
| `.bind <module> <key>` | Bind a module to a key |
| `.friend add <name>` | Add a player to your friend list |
| `.config load <name>` | Load an online configuration |
| `.panic` | Disable all active modules |
| `.client prefix <prefix>` | Change the command prefix |
| `.ping` | Show your current ping |
| `.coordinates` | Show your current position |

### Usage

Type commands in the Minecraft chat window. The command prefix (default: `.`) must be the first character. Arguments in `<angle brackets>` are required, and arguments in `[square brackets]` are optional.

```
.toggle KillAura
.bind Speed left.alt
.friend add SenkJu
.friend add SenkJu "Senk Ju"
.value set modules.killaura.range 4.5
.value set settings.commands.prefix !
```

> **Note:** Use double quotes around arguments that contain spaces, for example `.friend add SenkJu "Senk Ju"`.

> Minecraft usernames cannot contain spaces — the example `.friend add "Senk Ju"` as a username is invalid. Quotes are useful for aliases or display names when the command supports them.

**Total: 40 commands**
