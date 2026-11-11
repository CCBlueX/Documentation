## Commands

Sets how you type [commands](/docs/commands/overview) in chat.

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Prefix | Text | `.` | | What every command starts with. With `.` you type `.toggle KillAura`. |
| HintCount | Integer | 5 | 0 to 10 | When you mistype a command, the chat suggests this many commands with a similar name. 0 turns the suggestions off. |

You can also change the prefix with `.client prefix`. For example, `.client prefix !` makes commands start with `!`, so you would type `!help`.

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/command/CommandManager.kt)*
