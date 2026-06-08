## ItemTags

ItemTags renders floating overlay tags above dropped item entities in the world, showing each item's icon and stack count at a glance. Instead of having to walk up to a pile of drops and check them one by one, you can see exactly what's on the ground — and how much of it — directly in your HUD. This is especially handy after a big fight, a mob farm run, or any situation where a lot of items have scattered across the floor.

You can use the **Filter** setting to either whitelist specific items you care about (so only those show tags) or blacklist items you want to hide from the display. Nearby item entities can be automatically grouped into a single tag cluster based on distance, and duplicate stacks can be merged into a combined count to keep the display tidy. For dropped shulker boxes, an optional sub-display can expand and show the contents stored inside them, complete with an optional title label.

Tags scale with distance and support overlap prevention so they don't pile on top of each other. You can nudge the tag position with **RenderOffset** if you want them to appear higher or lower relative to the item, and adjust **RowLength** to control how many item icons appear per row before wrapping.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Filter | Choice | Blacklist | Whitelist, Blacklist | Whether the Items list acts as a whitelist (only show tags for listed items) or a blacklist (hide tags for listed items, show all others). |
| Items | Registry List | — | — | The list of items used by the Filter setting. |
| BackgroundColor | Color | — | — | Background color of the tag boxes drawn behind item icons. |
| Scale | Curve | — | — | Controls tag scale as a function of distance from the camera. |
| RenderOffset | Vector3_d | — | — | Positional offset applied to each tag's anchor point in world space, allowing fine-tuned vertical or horizontal adjustment. |
| RowLength | Integer | 100 | 1–100 | Maximum number of item icons per row in a tag box before wrapping to the next row. |
| PreventOverlap | Toggle | true | — | When enabled, tags are repositioned to avoid overlapping each other on screen. |
| ClusterEntities | Curve | — | — | Controls the clustering radius as a function of distance; item entities within this radius are grouped under one shared tag. |
| MergeMode | Choice | ByComponents | None, ByItem, ByComponents | How stacks within a cluster are merged: **None** keeps every stack separate, **ByItem** combines stacks of the same item type, **ByComponents** combines stacks that share the same item type and all data components (e.g. enchantments, custom names). |
| Shulker | Toggleable Group | off | — | When enabled, dropped shulker boxes also display a secondary tag showing their stored contents. |
| Shulker → MergeStacks | Toggle | true | — | When enabled, the shulker contents display applies the active MergeMode to combine duplicate stacks inside the box. |
| Shulker → ShowTitle | Toggle | true | — | When enabled, the shulker contents display includes the shulker box's name as a title above the contents. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleItemTags.kt)*
