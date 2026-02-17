## Commands

Configures the command system prefix and behavior.

### Settings

```
├── Prefix (Text | default: ".")
└── HintCount (Integer | default: 5 | range: 0..10)
```

### Settings Details

- **Prefix** (Text) — default: `"."` — The character(s) that must precede every command. For example, with the default prefix `.`, you would type `.toggle KillAura` in chat. You can change the prefix using the `.client prefix <newprefix>` command.
- **HintCount** (Integer) — default: `5`; range: `0` – `10` — When you type an unknown command, the client suggests similar commands. This setting controls how many suggestions are shown. Set to `0` to disable hints.

### Usage

All commands are typed in the Minecraft chat and must begin with the configured prefix. For example:

```
.toggle KillAura
.help
.friend add Steve
```

If you type an unrecognized command, the client will show up to **HintCount** similar commands to help you find what you were looking for.

> **Tip:** You can change the prefix at any time using `.client prefix <newprefix>`. For example, `.client prefix !` changes the prefix to `!`.
