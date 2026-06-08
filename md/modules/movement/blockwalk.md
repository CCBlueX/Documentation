## BlockWalk

BlockWalk lets you walk across blocks that aren't full cubes as if they had a solid, full-height top surface. Normally blocks like cobwebs or snow layers have a reduced or sticky collision shape that slows you down or lets you sink in; BlockWalk replaces their collision shape with a standard full-block shape so you can move over them cleanly.

It works by intercepting the collision-shape calculation for blocks in your configured list and swapping in a full cube shape — see [the shape handler](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleBlockWalk.kt#L39-L44). By default it targets cobwebs and snow, but you can edit the **Blocks** list to add or remove any blocks you want to treat as walkable. Use it when you want consistent footing over partial blocks instead of getting caught or slowed by their real hitboxes.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Blocks | Registry List | Cobweb, Snow | — | The blocks whose collision shape is replaced with a full block, letting you walk on top of them. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleBlockWalk.kt)*
