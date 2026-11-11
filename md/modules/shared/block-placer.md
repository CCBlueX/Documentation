## Block Placer

The Block Placer settings control how a module places blocks for you: how far it reaches, how fast it places and whether you turn to look at the block. Some modules give this group another name, like Placer or Placing, but the settings are the same.

A block is not placed where a player, mob, boat, minecart or end crystal is in the way. Dropped items, arrows and experience orbs do not stop it.

Used by: [AutoBuild](/docs/modules/world/autobuild), [BedDefender](/docs/modules/world/beddefender), [BlockIn](/docs/modules/world/blockin), [BlockTrap](/docs/modules/world/blocktrap), [HoleFiller](/docs/modules/world/holefiller), [LiquidFiller](/docs/modules/world/liquidfiller), [Surround](/docs/modules/world/surround), [CrystalAura](/docs/modules/combat/crystalaura) (BasePlace).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal | 4.5 | 1.0..6.0 | How far away you can place blocks, in blocks. |
| WallRange | Decimal | 4.5 | 0.0..6.0 | How far away you can place blocks you can't see. 0 means only blocks you can see. |
| Cooldown | Integer Range | 1..2 | 0..40 ticks | How long to wait between placing blocks, in ticks (20 per second). |
| Swing | Choice | DoNotHide | DoNotHide, HideForClient | Whether you see your arm swing when placing. |
| ConstructFailResult | Toggle | true | | Places the block even when it can't find a perfect spot to click. Works on most servers and makes placing much more reliable. |
| Sneak | Integer Range | 1..1 | 0..10 ticks | How long to sneak when placing on a block you could open, like a chest, so it does not open. |
| Ignore | Multi-Select | OpenInventory, UsingItem | OpenInventory, UsingItem | Keeps placing while a chest or your inventory is open (OpenInventory) or while you use an item (UsingItem). Remove one to stop placing at that time. |
| SlotResetDelay | Integer Range | 4..6 | 0..40 ticks | How long to wait before switching back to your old item. |
| RotationMode | Choice | Normal | Normal, None | Whether you look at the block you place. Normal turns you, see [Shared: Rotations](/docs/modules/shared-settings/rotations). None does not turn you. |
| RotationMode → PostMove | Toggle | false | | Turns after you move instead of before. |
| RotationMode → [None] → SendRotationPacket | Toggle | false | | Still tells the server where you would look. |
| RotationMode → [None] → Placements | Integer | 1 | 1..10 | How many blocks to place at once. |
| Support | Toggleable Group | On | | When there is nothing to place a block against, it first places other blocks to build up to it. Not in every module. |
| Support → Depth | Integer | 4 | 1..12 | How many extra blocks it may place for this. |
| Support → Delay | Integer | 500 | 0..1000 ms | How often it looks for a way to build up. |
| Support → Filter | Choice | Blacklist | Whitelist, Blacklist | Whitelist only uses the blocks in the list. Blacklist uses every block except those. |
| Support → Blocks | Registry List | | | The blocks for the filter. |
| DestroyCrystals | Toggleable Group | On | | Breaks end crystals that are in the way. |
| DestroyCrystals → Range | Decimal | 4.5 | 1.0..6.0 | How far away you can hit crystals. |
| DestroyCrystals → WallRange | Decimal | 4.5 | 0.0..6.0 | How far away you can hit crystals behind blocks. |
| DestroyCrystals → Delay | Integer | 0 | 0..1000 ms | How long to wait between hits. |
| DestroyCrystals → SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Whether your arm swing is shown to you, the server, both or nobody. |
| DestroyCrystals → RotationMode | Choice | Normal | Normal, None | Whether you turn toward the crystal. |
| TargetRendering | Toggleable Group | Off | | Shows the blocks it is about to place. See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |
| PlacedRendering | Toggleable Group | On | | Shows the blocks it just placed for a moment. See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/block/placer/BlockPlacer.kt)*
