## Spammer

Spammer sends chat messages again and again while it's on. The messages come from a list in the settings or from a text file with one message per line. Changes to the file are picked up without choosing it again. Messages longer than 256 characters are skipped. The module turns off when you leave a server.

To get past simple chat filters, it changes each message a little. With CustomFormatter off, it puts a few random letters in front and mixes upper and lower case. With CustomFormatter on, you decide yourself: `%f` becomes a random decimal number, `%i` a random number, `%s` a random word and `@a` the name of a random online player. Then MessageConverter changes the text once more.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Delay | Decimal Range | 2.0..4.0 | 0.0..300.0 secs | Wait between rounds. |
| MPS | Integer Range | 1..1 | 1..500 messages | How many messages to send each round. |
| MessageSource | Mode Selector | Setting | Setting, File | Take messages from the list below or from a file. |
| MessageSource → [Setting] → Message | Editable List | Four LiquidBounce ads | | Messages to send. |
| MessageSource → [File] → Source | File | | | A `.txt` file with one message per line. |
| Pattern | Choice | Random | Random, Linear | Random picks any message. Linear goes through them in order. |
| MessageConverter | Choice | Leet | None, Leet, Random Case, Random Space | Leet swaps some letters for numbers. Random Case mixes upper and lower case. Random Space adds spaces. |
| CustomFormatter | Toggle | false | | Lets you use `%f`, `%i`, `%s` and `@a` in messages. Messages starting with `/` are only sent as commands when this is on. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleSpammer.kt)*
