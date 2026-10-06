## BlockTrap

BlockTrap surrounds a nearby enemy with blocks to box them in place, making it hard for them to move, escape, or fight back. It targets the closest valid player (by view direction, within range) and builds a cage around their hitbox automatically. Use it in close-quarters PvP when you want to lock an opponent down — for example to set up combos or to deny them an escape route.

Under the hood, the module scans the area around the target's bounding box and selects the positions that wrap the sides of the hitbox while skipping the spots that are inside the box or only touch it on a single axis — see [the trap-plan logic](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBlockTrap.kt#L106-L140). It then trims and extends that plan based on your `PlaceAt` and `DoublePlace` options before handing the positions to the shared block placer. With `Instant` enabled, the module immediately re-places any block the enemy manages to break, using the [instant re-place on block update](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBlockTrap.kt#L97-L104) handler.

The blocks actually used for placement are drawn from your hotbar according to the `Filter` and `Blocks` list, and the order in which positions are queued is controlled by `PlacePriority`.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| DoublePlace | Multi-Select | [] | [Above, Below] | Adds a second layer of blocks. **Above** places two blocks above the target's head so they can't mine the block and tower up to escape at the same time. **Below** places a second layer beneath the target so they can't mine the block under them and fall through (requires **Floor** in PlaceAt). |
| PlaceAt | Multi-Select | [Legs, Floor] | [Legs, Floor] | Which layers around the target to include. **Legs** allows placing at the target's leg level; **Floor** allows placing at the floor level. Disabling one filters those positions out of the plan. |
| Instant | Toggle | true | — | Instantly re-places any trap block the target breaks, reacting to block-update packets. Requires the rotation mode "None" in the block placer. |
| Filter | Choice | Blacklist | [Whitelist, Blacklist] | How the **Blocks** list is interpreted. **Whitelist** uses only the listed blocks; **Blacklist** uses any block except the listed ones. |
| Blocks | Registry List | — | — | The list of blocks that the Filter applies to when selecting which item to place from your hotbar. |
| PlacePriority | Choice | Furthest | [Closest, Furthest, Highest, Lowest] | Order in which positions are added to the placement queue. **Closest**/**Furthest** sort by distance from you; **Highest**/**Lowest** sort by Y level. |
| Place | Setting Group | — | — | See [Shared: Block Placer](/docs/modules/shared-settings/block-placer). |
| Target | Setting Group | — | — | See [Shared: Target](/docs/modules/shared-settings/target). |
| TargetRendering | Toggleable Group | on | — | See [Shared: TargetRendering](/docs/modules/shared-settings/target-rendering). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleBlockTrap.kt)*
