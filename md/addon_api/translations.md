## Translations

The client looks up the descriptions of modules, settings and commands by translation key. An add-on ships its own keys in JSON files, one per language.

### Files

Translations go into `src/main/resources/resources/<id>/lang/<code>.json`, where `<id>` is the add-on id:

```json
{
  "liquidbounce.module.greeter.description": "Greets a friend when enabled.",
  "liquidbounce.module.greeter.friend.description": "Who to greet.",
  "liquidbounce.module.greeter.sound.description": "Play a sound as well.",
  "liquidbounce.module.greeter.sound.volume.description": "How loud.",
  "liquidbounce.module.greeter.messages.hello": "Hello, %s!",
  "example-addon.farewell": "Goodbye."
}
```

The client knows these languages:

| Code    | Language              |
|---------|-----------------------|
| `en_us` | English (US)          |
| `en_pt` | English (Pirate)      |
| `de_de` | German                |
| `ja_jp` | Japanese              |
| `zh_cn` | Chinese (Simplified)  |
| `zh_tw` | Chinese (Traditional) |
| `ru_ru` | Russian               |
| `ua_ua` | Ukrainian             |
| `pt_br` | Portuguese (Brazil)   |
| `tr_tr` | Turkish               |
| `nl_nl` | Dutch (Netherlands)   |
| `nl_be` | Dutch (Belgium)       |

A key missing in the player's language falls back to `en_us`, and to the key itself if that has none either. Ship `en_us.json` at least; a module without an `en_us` description logs a warning when it is registered.

The add-on's keys are merged into the client's. A key that is already defined, by the client or an earlier add-on, keeps its text, so an add-on cannot change a built-in string.

### Keys

The client derives the keys from the names, each converted to lower camel case (`JumpCounter` becomes `jumpCounter`):

| Key                                                              | Used for                                            |
|------------------------------------------------------------------|-----------------------------------------------------|
| `liquidbounce.module.<module>.description`                       | The module's description.                           |
| `liquidbounce.module.<module>.<setting>.description`             | A setting's description.                            |
| `liquidbounce.module.<module>.<group>.<setting>.description`     | A setting inside a nested group, and so on for deeper nesting. |
| `liquidbounce.module.<module>.<modes>.<mode>.<setting>.description` | A setting of a [mode](/docs/add-on-api/developers/creating-modules#modes), `<modes>` being the name passed to `choices`. |
| `liquidbounce.module.<module>.messages.<key>`                    | `message(key, args)` in the module.                 |
| `liquidbounce.command.<command>.description`                     | The command's description, shown by `.help`.        |
| `liquidbounce.command.<command>.<key>`                           | `t(key, args)` in the [command DSL](/docs/add-on-api/developers/creating-commands). |

A group or a mode selection has a description of its own too, under `<...>.<group>.description`.

For this module, the file above covers the module, its settings, the group and its message:

```kotlin
object ModuleGreeter : ClientModule("Greeter", ModuleCategories.MISC) {

    private val friend by text("Friend", "Steve")

    private object Sound : ToggleableValueGroup(this, "Sound", false) {
        val volume by float("Volume", 1f, 0f..1f)
    }

    init {
        tree(Sound)
    }

    override fun onEnabled() {
        chat(message("hello", friend), this)
    }

}
```

### Using translations

`translation(key, args)` returns a `MutableComponent` for any key, with `args` filling `%s` placeholders:

```kotlin
chat(translation("example-addon.farewell"))
```

Keys outside `liquidbounce.module` and `liquidbounce.command` are free to use; prefixing them with the add-on id keeps them apart from other add-ons.

A description can also be set without a translation, with `literalDescription { "..." }` on the module or setting.
