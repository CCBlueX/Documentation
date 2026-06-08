## LiquidFiller

LiquidFiller automatically places blocks inside liquid source blocks — water, lava, or both — that are within your reach. This lets you drain or pave over bodies of liquid without manually placing each block, making it handy for building in oceans, clearing lava lakes in the Nether, or quickly flooding-prevention on survival servers.

The **Blocks** registry list, combined with the **Filter** setting, controls which items in your inventory are eligible for placement. In Whitelist mode only the listed blocks are used; in Blacklist mode every block in your inventory is fair game except those on the list. If **UseSponge** is enabled, LiquidFiller will place a sponge instead of a regular block when targeting water — sponges absorb a large surrounding area in one go, which can be far more efficient than filling individual source blocks one at a time.

**PlaceOrder** determines the sequence in which discovered liquid positions are filled. The default **FurtherFirst** works outward first, which tends to prevent the liquid from flowing back toward you as you fill. Switch to **CloserFirst** if you want to clear the area immediately around you first, or use **BottomTop**/**TopBottom** to fill layer by layer vertically.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| PlaceIn | Multi-Select | Water, Lava | — | Which liquid types to target. Select Water, Lava, or both. |
| PlaceOrder | Choice | FurtherFirst | Random, CloserFirst, FurtherFirst, BottomTop, TopBottom | Order in which liquid source blocks are filled. |
| UseSponge | Toggle | false | — | When enabled, places a sponge to absorb nearby water source blocks instead of filling them individually. Requires a sponge in your hotbar or offhand. |
| Filter | Choice | Whitelist | Whitelist, Blacklist | Whether the Blocks list acts as a whitelist (only use listed blocks) or a blacklist (use any block except those listed). |
| Blocks | Registry List | — | — | The blocks considered for filling liquids, interpreted according to the Filter setting. |
| Placer | Setting Group | — | — | See [Shared: Block Placer](/docs/modules/shared-settings/block-placer). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleLiquidFiller.kt)*
