## AutoConfig

AutoConfig loads a config from the marketplace when you join a server. It picks the best-rated config made for that server, and a notification tells you if one was loaded, if none exists, or if loading failed. If you turn it on while you're already on a server, it loads the config for that server right away.

The module's name in the array list shows the loaded config as `author/name`, with a `*` after it once you change a setting. If you rejoin, your changes stay. After you load your own config with `.localconfig load`, AutoConfig keeps that one and stops loading server configs.

See [Configs](/docs/usage/configs) to load, report or publish configs yourself.

**Category:** Misc
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| OnlyFeatured | Toggle | true | | Only loads configs picked by the LiquidBounce team. Turn it off to also load configs made by other players. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoConfig.kt)*
