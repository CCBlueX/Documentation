## ChestStealer

ChestStealer takes the items out of a chest or other container as soon as you open it, much faster than clicking by hand. Use it for looting in games like SkyWars or Bedwars.

It takes everything, unless [InventoryCleaner](/docs/modules/player/inventorycleaner) is on. Then it only takes items you want to keep and throws away junk when your inventory is full. **Aura** opens chests near you by itself, and **SilentScreen** loots without the chest screen covering your view.

**Category:** Player
**Enabled by default:** No

### Settings

Some settings are in ticks (20 per second).

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Constraints | Setting Group | | | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| AutoClose | Toggle | true | | Closes the container when it has taken everything. |
| SelectionMode | Mode Selector | Distance | Distance, Index, Random | The order items are taken in. Distance goes to the nearest slot next, Index goes slot by slot, Random picks any. |
| SelectionMode → [Distance] → StartItem | Choice | Default | Default, Random, MaxSlot, MinSlot | Which item to start with. |
| SelectionMode → [Distance] → RandomFactor | Decimal Range | 1.0..1.0 | 0.25..2.0 | Mixes up the order a bit. 1.0..1.0 means no change. |
| SelectionMode → [Index] → Order | Choice | Ascending | Ascending, Descending | Start from the first slot or the last one. |
| MoveMode | Choice | QuickMove | QuickMove, DragAndDrop | QuickMove shift-clicks items. DragAndDrop picks them up and puts them down, for servers where shift-click doesn't work. |
| QuickSwaps | Toggle | true | | Moves items like swords straight to your hotbar instead of shift-clicking them, because some servers flag that. |
| OnFull | Choice | Throw | None, Throw | What to do when your inventory is full: stop, or throw away useless items to make room. |
| CheckScreenHandlerType | Toggleable Group | On | | See [Shared: CheckScreenHandlerType](/docs/modules/shared-settings/checkscreenhandlertype). |
| CheckScreenTitle | Toggleable Group | On | | See [Shared: CheckScreenTitle](/docs/modules/shared-settings/checkscreentitle). |
| Aura | Toggleable Group | On | | Opens storage blocks near you by itself. |
| Aura → Range | Decimal | 3.0 | 1.0..6.0 | How far away a block can be, in blocks. |
| Aura → WallRange | Decimal | 0.0 | 0.0..6.0 | How far away a block behind a wall can be. Can't be more than Range. |
| Aura → Delay | Integer | 5 | 1..80 ticks | Wait between opening blocks. |
| Aura → SwingMode | Choice | DoNotHide | DoNotHide, HideForClient | Whether you see your own arm swing. |
| Aura → NotDuringCombat | Toggle | true | | Doesn't open blocks while you are fighting. |
| Aura → TrackManualInteractions | Toggle | true | | Remembers chests you opened yourself, so it doesn't open them again. |
| Aura → PauseOn | Multi-Select | | Combat, UsingItem | Pauses while you are fighting or using an item. |
| Aura → ValidStorageBlocks | Registry List | All chests, shulker boxes, barrels and furnaces, Brewing Stand, Dispenser, Hopper | | Blocks it opens. |
| Aura → AwaitContainer | Toggleable Group | On | | Waits for the screen to open and tries again if it doesn't. |
| Aura → AwaitContainer → Timeout | Integer | 10 | 1..80 ticks | How long to wait before trying again. |
| Aura → AwaitContainer → MaxRetries | Integer | 4 | 1..10 | How often to try before skipping the block. |
| Aura → Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| SilentScreen | Toggleable Group | Off | | Loots without showing the chest screen, so you can keep moving and looking around. |
| SilentScreen → UnlockCursor | Toggle | false | | Shows your mouse cursor while it loots. |
| SilentScreen → DrawInventoryTag | Toggleable Group | On | | Shows the chest's items floating over the block. |
| SilentScreen → DrawInventoryTag → Background | Mode Selector | Rect | Rect, Texture | What is drawn behind the items. |
| SilentScreen → DrawInventoryTag → Background → [Rect] → Color | Color | | | Fill color. |
| SilentScreen → DrawInventoryTag → Background → [Rect] → OutlineColor | Color | | | Outline color. |
| SilentScreen → DrawInventoryTag → Background → [Rect] → Margin | Decimal | 2.0 | 0.0..100.0 | Space between the items and the edge. |
| SilentScreen → DrawInventoryTag → Background → [Rect] → Radius | Decimal | 4.0 | 0.0..16.0 | How round the corners are. |
| SilentScreen → DrawInventoryTag → Background → [Rect] → Gradient | Decimal | 0.3 | 0.0..1.0 | How strong the color fade is. |
| SilentScreen → DrawInventoryTag → Background → [Rect] → Glow | Decimal | 0.3 | 0.0..1.0 | How strong the glow is. |
| SilentScreen → DrawInventoryTag → Scale | Decimal | 1.5 | 0.25..4.0 | Size of the floating items. |
| SilentScreen → DrawInventoryTag → RenderOffset | Vector | | | Moves the floating items away from the block. |
| SilentScreen → DrawInventoryTag → ShowTitle | Toggle | false | | Shows the container's name above the items. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/cheststealer/ModuleChestStealer.kt)*
