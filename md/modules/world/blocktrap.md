## BlockTrap

BlockTrap builds a box of blocks around a nearby enemy so they get stuck. Use it in close fights when you want to stop someone from running away.

It uses blocks from your hotbar. With Instant on, it puts back blocks the enemy breaks right away.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| DoublePlace | Multi-Select | None | Above, Below | Above: puts two blocks over the enemy's head, so they can't break out and build up. Below: puts two layers under them, so they can't dig down (needs Floor in PlaceAt). |
| PlaceAt | Multi-Select | Legs, Floor | Legs, Floor | Legs: places blocks at the enemy's leg height. Floor: places blocks under them. |
| Instant | Toggle | true | | Puts back broken trap blocks right away. Only works when the Rotations mode in Place is None. |
| Filter | Choice | Blacklist | Whitelist, Blacklist | Whitelist: only use the listed blocks. Blacklist: use any block except the listed ones. |
| Blocks | Registry List | | | The blocks the filter uses. |
| PlacePriority | Choice | Furthest | Closest, Furthest, Highest, Lowest | Which blocks go down first: closest or furthest from you, highest or lowest. |
| Place | Setting Group | | | See [Block Placer](/docs/modules/shared-settings/block-placer). |
| Target | Setting Group | | | See [Target](/docs/modules/shared-settings/target). |
| Target → Range | Decimal | 4.0 | 1.0..6.0 blocks | How close an enemy has to be. |
| TargetRendering | Toggleable Group | On | | See [Target Rendering](/docs/modules/shared-settings/targetrendering). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBlockTrap.kt)*
