## AutoBuild

AutoBuild builds things for you with blocks from your hotbar. Pick what to build with Mode and turn it on. It turns itself off when it is done.

Portal builds and lights a Nether portal near you. You need obsidian and flint and steel. Platform places a flat square of blocks under your feet, for example to cover a hole.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Portal | Portal, Platform | What to build. |
| Mode → [Portal] → IgniteTimeout | Integer | 2000 | 200..10000 ms | How long it tries to light the portal before it gives up. |
| Mode → [Platform] → DisableOnYChange | Toggle | true | | Turns off when you move up or down. |
| Mode → [Platform] → Filter | Choice | Whitelist | Whitelist, Blacklist | Whitelist uses only the listed blocks. Blacklist uses every block except them. |
| Mode → [Platform] → Blocks | Registry List | Obsidian | | The blocks the filter uses. |
| Mode → [Platform] → Size | Integer | 3 | 1..6 | How big the platform is. |
| Placing | Setting Group | | | See [Block Placer](/docs/modules/shared-settings/block-placer). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/autobuild/ModuleAutoBuild.kt)*
