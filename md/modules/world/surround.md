## Surround

Surround places obsidian around your feet so you stand in a safe hole. End crystals do much less damage to you there, so it is used in Crystal PvP. It turns off when you jump or get knocked out of the hole.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Features | Multi-Select | Extend, Down | Center, Extend, NoWaste, Down | Center moves you to the middle of your block. Extend builds around players or mobs standing in the way. NoWaste builds nothing bigger if you are already in a full 1x1 hole. Down also places a block under you. |
| DisableOn | Multi-Select | YChange | YChange, XZMove, XZSpeed | When to turn off: when you move up or down, move more than half a block, or move fast. |
| Instant | Toggle | true | | Replaces a broken block right away. Needs the rotation mode under Placing set to None. |
| Protect | Toggleable Group | On | | Reacts when someone mines your blocks. |
| Protect → MinDestroyProgress | Integer | 4 | 0..9 stage | How far the block has to be mined (0 to 9) before it reacts. |
| Protect → ExtraLayer | Toggleable Group | On | | Builds another layer outside the block being mined. |
| Protect → ExtraLayer → Corners | Toggle | false | | Also fills the corners. |
| AddExtraLayer | Key | | | Hold this key to always build the extra layer. |
| Filter | Choice | Whitelist | Whitelist, Blacklist | Whitelist uses only the listed blocks. Blacklist uses every block except them. |
| Blocks | Registry List | Obsidian, Ender Chest, Crying Obsidian | | The blocks the filter uses. |
| Placing | Setting Group | | | See [Block Placer](/docs/modules/shared-settings/block-placer). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleSurround.kt)*
