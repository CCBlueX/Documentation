## ChestStealer

ChestStealer empties chests and other containers for you the moment you open them, shift-clicking (or dragging) every worthwhile item into your inventory in a fraction of a second. It's built for loot runs where speed matters, like grabbing chests on Bedwars, SkyWars, or while raiding bases.

By default it simply takes everything, but if [InventoryCleaner](/docs/modules/player/inventorycleaner) is running, ChestStealer follows that module's plan instead — only pulling items you actually want, merging stacks, and throwing away junk to free space when your inventory is full. The built-in **Aura** can also open nearby storage blocks automatically so you can chain through rows of chests without clicking, and **SilentScreen** lets the whole thing happen without the container GUI blocking your view.

To keep things looking natural and to avoid grabbing from the wrong window, you can restrict it to genuine containers by handler type and title, and quick-swap risky items (like swords) straight out of the chest because some servers dislike rapid shift-clicks on those.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Constraints | Setting Group | — | — | See [Shared: Inventory Constraints](/docs/modules/shared-settings/inventory-constraints). |
| AutoClose | Toggle | true | — | Closes the container screen automatically once everything worth taking has been grabbed. |
| SelectionMode | Choice | Distance | Distance, Index, Random | Order items are pulled in — Distance follows a nearest-neighbour path across the slots, Index goes slot by slot, Random shuffles for a less predictable pattern. |
| MoveMode | Choice | QuickMove | QuickMove, DragAndDrop | How items are transferred — QuickMove shift-clicks each stack, DragAndDrop picks up and drops stacks manually (handy where shift-click is restricted). |
| QuickSwaps | Toggle | true | — | Hotbar-swaps items such as swords straight out of the chest instead of shift-clicking them, since some servers flag that behaviour. |
| OnFull | Choice | Throw | None, Throw | What to do when your inventory fills before the chest is empty — None stops, Throw drops useless items to make room. |
| CheckScreenHandlerType | Toggleable Group | On | — | See [Shared: CheckScreenHandlerType](/docs/modules/shared-settings/checkscreenhandlertype). |
| CheckScreenTitle | Toggleable Group | On | — | See [Shared: CheckScreenTitle](/docs/modules/shared-settings/checkscreentitle). |
| Aura | Toggleable Group | On | — | Automatically interacts with nearby storage blocks to open them, so you can chain through chests hands-free. |
| Aura → Range | Decimal | 3.0 | 1.0–6.0 | How far away (in blocks) a storage block can be for the aura to open it. |
| Aura → WallRange | Decimal | 0.0 | 0.0–6.0 | Reach for storage blocks you don't have line of sight to; capped at the Range value. |
| Aura → Delay | Integer | 5 | 1–80 ticks | Wait time between opening one block and the next. |
| Aura → SwingMode | Choice | DoNotHide | DoNotHide, HideForBoth, HideForClient, HideForServer | Whether and where the hand-swing animation is shown when opening a block. |
| Aura → NotDuringCombat | Toggle | true | — | Pauses opening blocks while you're in combat. |
| Aura → TrackManualInteractions | Toggle | true | — | Remembers chests you open yourself so the aura won't immediately reopen them. |
| Aura → PauseOn | Multi-Select | None | Combat, UsingItem | Conditions that temporarily halt the aura. |
| Aura → ValidStorageBlocks | Registry List | — | — | Which block types count as storage and will be opened. |
| Aura → AwaitContainer | Toggleable Group | On | — | Waits for the container screen to actually open before moving on, retrying if it doesn't. |
| Aura → AwaitContainer → Timeout | Integer | 10 | 1–80 ticks | How long to wait for the screen to appear before retrying. |
| Aura → AwaitContainer → MaxRetries | Integer | 4 | 1–10 | How many times to retry opening a block before giving up on it. |
| Aura → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| SilentScreen | Toggleable Group | Off | — | Steals from the container without the inventory GUI taking over your screen, so you can keep moving and looking around. |
| SilentScreen → UnlockCursor | Toggle | false | — | Frees your mouse cursor while the silent screen is active. |
| SilentScreen → DrawInventoryTag | Toggleable Group | On | — | Renders the container's contents as a floating overlay at the block's position. |
| SilentScreen → DrawInventoryTag → Background | Mode Selector | Rect | Rect, Texture | Style drawn behind the floating item overlay. |
| SilentScreen → DrawInventoryTag → Background → [Rect] → Color | Color | — | — | Fill colour of the rectangle background. |
| SilentScreen → DrawInventoryTag → Background → [Rect] → OutlineColor | Color | — | — | Outline colour of the rectangle background. |
| SilentScreen → DrawInventoryTag → Background → [Rect] → Margin | Decimal | 2.0 | 0.0–100.0 | Padding between the items and the edge of the rectangle. |
| SilentScreen → DrawInventoryTag → Scale | Decimal | 1.5 | 0.25–4.0 | Size of the floating overlay. |
| SilentScreen → DrawInventoryTag → RenderOffset | Vector3_d | — | — | Position offset of the overlay relative to the block. |
| SilentScreen → DrawInventoryTag → ShowTitle | Toggle | false | — | Shows the container's title above the overlay. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/cheststealer/ModuleChestStealer.kt)*
