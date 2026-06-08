## Block Placer

The Block Placer setting group controls how a module places blocks into the world — the reach, timing, rotations, and how placements are visualized. It is shared by every module that automatically places blocks, so the placement behaviour is configured the same way everywhere.

The Block Placer setting group appears in the following modules:
- [AutoBuild](/docs/modules/world/autobuild)
- [BedDefender](/docs/modules/world/beddefender)
- [BlockIn](/docs/modules/world/blockin)
- [BlockTrap](/docs/modules/world/blocktrap)
- [HoleFiller](/docs/modules/world/holefiller)
- [LiquidFiller](/docs/modules/world/liquidfiller)
- [Surround](/docs/modules/world/surround)
- [CrystalAura](/docs/modules/combat/crystalaura) (placement sub-module)

Some modules rename the group (for example LiquidFiller calls it **Placer**), but the settings are the same.

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Range | Decimal | 4.5 | 1.0–6.0 | Maximum reach, in blocks, for placements you can see directly. |
| WallRange | Decimal | 4.5 | 0.0–6.0 | Maximum reach for placements that are not in your direct line of sight (e.g. behind or around blocks). Set to 0 to only place visible blocks. |
| Cooldown | Integer Range | 1..2 | 0..40 ticks | Delay between placements. A random value within this range is chosen each time. |
| Swing | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Whether the hand-swing animation is shown to you, the server, both, or neither. |
| ConstructFailResult | Toggle | true | — | When the placement raytrace fails, fall back to a constructed center-hit instead of skipping. Makes placements much more reliable on most servers, at the cost of slightly less accurate rotations and reach. |
| Sneak | Integer Range | 1..1 | 0..10 ticks | How long to keep sneaking when placing against an interactable block (chest, furnace, etc.) so it is not opened instead of built on. |
| Ignore | Multi-Select | [] | OpenInventory, UsingItem | Situations in which the module should keep placing anyway: while an inventory is open, and/or while you are using an item. |
| SlotResetDelay | Integer Range | 4..6 | 0..40 ticks | Delay before switching your hotbar slot back after a placement. |
| RotationMode | Mode | Normal | Normal, NoRotation | **Normal** rotates toward each placement using the shared [Rotations](/docs/modules/shared/rotations) settings. **NoRotation** places without rotating (the server is not told you looked at the block). |
| Support | Toggleable Group | off* | — | Places a support block first when the target position has nothing to place against. *Only available in modules that allow support placements; disabled and hidden otherwise.* |
| CrystalDestroyer | Toggleable Group | — | — | Destroys end crystals that are blocking a placement before placing. |
| TargetRendering | Toggleable Group | — | — | Renders the positions that are queued to be placed. Uses the [TargetRendering](/docs/modules/shared/target-rendering)-style placement renderer. |
| PlacedRendering | Toggleable Group | — | — | Renders positions that were just placed (fades out). |

> For rotation tuning, see [Rotations](/docs/modules/shared/rotations). For the placement preview boxes, see [TargetRendering](/docs/modules/shared/target-rendering).

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Futils%2Fblock%2Fplacer%2FBlockPlacer.kt)*
