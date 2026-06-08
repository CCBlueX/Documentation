## AutoConfig

AutoConfig takes the hassle out of switching settings between servers. Many servers run very different anticheats, so the configuration that works perfectly on one may flag you instantly on another. When AutoConfig is on, it looks at the server you're about to join and automatically applies the matching config from LiquidBounce's online config repository — so you're set up correctly before you even spawn in.

It kicks in the moment you connect to a server: it briefly holds the connection, finds the best-matching config for that server's address (preferring the most general config when several exist), and loads it while the connect screen shows the progress. You'll get an on-screen notification telling you whether a config was loaded, whether none exists for that server, or whether loading failed. You can also enable it while already in-game to apply the config for your current server on the spot.

A few servers known for anticheat testing are deliberately skipped, and you'll be told if no config is available for where you're playing. AutoConfig has no settings of its own — just turn it on and let it manage your configs for you.

**Category:** Misc
**Enabled by default:** No

### Settings

This module has no configurable settings.

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModuleAutoConfig.kt)*
