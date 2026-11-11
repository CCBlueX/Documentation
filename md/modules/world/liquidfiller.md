## LiquidFiller

LiquidFiller places blocks into water and lava source blocks near you. Use it to clear lava lakes or build in water without placing each block by hand.

With **UseSponge** it places a sponge on water instead, which soaks up a lot of water at once.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| PlaceIn | Multi-Select | Water, Lava | Water, Lava | Which liquids to fill. At least one must be picked. |
| PlaceOrder | Choice | FurtherFirst | Random, CloserFirst, FurtherFirst, BottomTop, TopBottom | Which spots get filled first. |
| UseSponge | Toggle | false | | Places a sponge on water. Needs a sponge in your hotbar or offhand. |
| Filter | Choice | Whitelist | Whitelist, Blacklist | Whitelist: only use the blocks in the list. Blacklist: use any block except those. |
| Blocks | Registry List | All wool, Dirt, Cobblestone, Stone, Netherrack, Diorite, Granite, Andesite | | Blocks for the Filter. |
| Placer | Setting Group | | | See [Block Placer](/docs/modules/shared-settings/block-placer). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleLiquidFiller.kt)*
