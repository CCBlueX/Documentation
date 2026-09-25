## AutoConfig

AutoConfig loads a config from the marketplace when you join a server. It holds the connection for a moment, looks up the best-ranked config made for that server and loads it while the connect screen shows the progress. A notification tells you whether a config was loaded, whether there is none for the server, or whether loading failed. Turning the module on while you are on a server loads the config for that server right away.

The module's tag in the array list shows the loaded config as `author/name`, followed by `*` once you changed one of its settings. When you rejoin a server whose config you edited, AutoConfig keeps your changes. After you load a local config with `.localconfig load`, the tag shows its name and joining a server keeps it instead of loading a config for that server. A few servers known for anticheat testing are skipped.

See [Configs](/docs/usage/configs) for loading, reporting and publishing configs by hand.

**Category:** Misc
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| OnlyFeatured | Boolean | On | — | Only loads configs featured by the LiquidBounce team. Turn it off to also load configs published by other players. |

---
*Last updated: 2026-09-23 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2d4c325dc/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoConfig.kt)*
