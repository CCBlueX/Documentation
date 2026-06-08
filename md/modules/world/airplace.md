## AirPlace

AirPlace lets you place blocks, spawn eggs, armor stands, and firework rockets in mid-air, without needing an existing block or surface to click against. Normally Minecraft only allows placement when you're aiming at a solid face; with this module enabled, you can build outward into empty space wherever you're looking.

By default a translucent preview box shows exactly where the block will land before you commit, so you can line up your placement precisely. You can also turn on a fixed placement range so blocks always appear at a set distance from your eyes rather than wherever your crosshair happens to hit.

This is handy for free-floating builds, quick platforms, or reaching spots that would otherwise need scaffolding. If you want blocks to also go down into water and lava, enable PlaceInLiquid — note that this defers to [LiquidPlace](/docs/modules/world/liquidplace) while that module is active to avoid conflicts.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| PlaceInLiquid | Toggle | false | — | Also allows placing into fluid blocks like water and lava, not just empty air. Yields to [LiquidPlace](/docs/modules/world/liquidplace) when that module is running. |
| Preview | Toggleable Group | On | — | Renders a box at the spot where your block will be placed so you can see it before committing. |
| Preview → OutlineOnly | Toggle | false | — | Shows only the outline of the preview box, leaving the inside transparent instead of filled. |
| Preview → Color | Color | — | — | Fill color of the preview box. |
| Preview → OutlineColor | Color | — | — | Color of the preview box's outline. |
| CustomRange | Toggleable Group | Off | — | Places blocks at a fixed distance from your eyes along your aim direction instead of at the spot your crosshair lands on. |
| CustomRange → Range | Decimal | 3.0 | 1.0..4.5 | How far in front of you blocks are placed when CustomRange is on. |
| CustomRange → ScrollAdjust | Toggleable Group | On | — | See [Shared: ScrollAdjust](/docs/modules/shared-settings/scrolladjust). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleAirPlace.kt)*
