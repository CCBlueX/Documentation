## AirPlace

AirPlace lets you place blocks in the air, with nothing next to them. It also works for spawn eggs, armor stands and fireworks. A see-through box shows where the block will go.

Turn on **CustomRange** if blocks should always go at the same distance in front of you.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Preview | Toggleable Group | On | | Shows a box where the block will go. |
| Preview → OutlineOnly | Toggle | false | | Only draws the edges of the box. |
| Preview → Color | Color | | | Fill color of the box. |
| Preview → OutlineColor | Color | | | Edge color of the box. |
| PlaceInLiquid | Toggle | false | | Also lets you place blocks in water and lava. Does nothing while [LiquidPlace](/docs/modules/world/liquidplace) is on. |
| CustomRange | Toggleable Group | Off | | Places blocks at a set distance in front of you. |
| CustomRange → Range | Decimal | 3.0 | 1.0..4.5 | How far in front of you blocks go. |
| CustomRange → ScrollAdjust | Toggleable Group | On | | See [ScrollAdjust](/docs/modules/shared-settings/scrolladjust). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleAirPlace.kt)*
