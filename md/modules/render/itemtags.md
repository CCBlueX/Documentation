## ItemTags

ItemTags shows a small box above items on the ground with each item's picture and how many there are. You can see what dropped without walking over to it, for example after a fight or at a mob farm.

Items lying close together share one box, and stacks of the same item are added up. Dropped shulker boxes can also show what is inside them. Use **Filter** and **Items** to choose which items get a tag.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Filter | Choice | Blacklist | Whitelist, Blacklist | Whether the Items list picks the items to show or the items to hide. |
| Items | Registry List | Empty | | The items used by Filter. |
| Background | Mode Selector | Rect | Rect, Texture | What the box behind the items looks like: a panel, or inventory slots. |
| Background → Rect → Color | Color | Black, alpha 128 | | Color of the panel. |
| Background → Rect → OutlineColor | Color | Transparent | | Color of the panel's outline. |
| Background → Rect → Margin | Decimal | 2.0 | 0.0 to 100.0 | Space between the items and the panel's edge. |
| Background → Rect → Radius | Decimal | 4.0 | 0.0 to 16.0 | How round the corners are. |
| Background → Rect → Gradient | Decimal | 0.3 | 0.0 to 1.0 | How much darker the panel gets toward the bottom. |
| Background → Rect → Glow | Decimal | 0.3 | 0.0 to 1.0 | How strong the glow around the panel is. |
| Scale | Curve | 1 at every distance | Distance 0 to 200, Scale 0.25 to 4 | How big the tags are at each distance. |
| RenderOffset | Vector | 0, 0, 0 | | Moves the tags away from the item. |
| RowLength | Integer | 100 | 1 to 100 | How many items fit in one row before a new row starts. |
| PreventOverlap | Toggle | true | | Moves tags so they do not cover each other. |
| ClusterEntities | Curve | 2 up close, 16 at 64 blocks, 24 at 200 blocks | Distance 0 to 200, Size 0.1 to 32 | How close items must be, at each distance, to share one tag. |
| MergeMode | Choice | ByComponents | None, ByItem, ByComponents | How stacks are added up. **None** keeps them apart, **ByItem** adds up the same item, **ByComponents** only adds up items that are exactly the same, including enchantments and names. |
| Shulker | Toggleable Group | Off | | Also shows what is inside dropped shulker boxes. |
| Shulker → MergeStacks | Toggle | true | | Adds up the items inside the shulker box using MergeMode. |
| Shulker → ShowTitle | Toggle | true | | Shows the shulker box's name above its items. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleItemTags.kt)*
