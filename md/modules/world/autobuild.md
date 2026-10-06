## AutoBuild

AutoBuild constructs structures for you automatically, placing blocks from your hotbar (or offhand) so you don't have to aim and click each one yourself. Pick a structure with the **Mode** setting and toggle the module on — it does the rest, then turns itself off once the build is finished.

In **Portal** mode it scans around you for the best spot to raise a nether portal, fills in the obsidian frame, and lights it with flint and steel. You'll need obsidian (and flint and steel) in your inventory; if either is missing, or there's no valid spot nearby, AutoBuild stops and tells you in chat. **Platform** mode instead lays a flat square of blocks beneath your feet — handy for bridging across gaps or covering a hole — using whichever block you allow through its filter. With **DisableOnYChange** on, it shuts off the moment your height changes so it won't keep placing once you've moved.

All the actual block placing — timing, rotations, reach, swing and how it interacts with your inventory — is handled by the shared [Block Placer](/docs/modules/shared-settings/block-placer) settings. If you want continuous bridging while you walk rather than fixed structures, see [Scaffold](/docs/modules/world/scaffold).

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Portal | Portal, Platform | Which structure to build: a nether portal frame, or a flat platform beneath you. |
| Mode → [Platform] → DisableOnYChange | Toggle | true | — | Automatically turns the module off if your vertical position changes, so it stops once you've moved off the platform. |
| Mode → [Platform] → Filter | Choice | Whitelist | Whitelist, Blacklist | Whether the block list below is treated as the only blocks allowed (Whitelist) or the only blocks forbidden (Blacklist). |
| Mode → [Platform] → Blocks | Registry List | — | — | The blocks the filter applies to when choosing what to place for the platform. |
| Mode → [Platform] → Size | Integer | 3 | 1..6 | How far the platform extends out from your position, making it larger or smaller. |
| Placing | Setting Group | — | — | See [Shared: Block Placer](/docs/modules/shared-settings/block-placer). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/autobuild/ModuleAutoBuild.kt)*
