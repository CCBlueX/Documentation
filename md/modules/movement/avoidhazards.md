## AvoidHazards

AvoidHazards keeps you from blundering into blocks that hurt you or otherwise mess with your movement — cacti, fire, lava, cobwebs, sweet berry bushes, magma blocks, wither roses, powder snow, pressure plates, and ladders. It's handy in PvP, parkour, and general survival when you're moving fast and don't want a stray cactus or a hidden lava pool to ruin your run.

The module works in one of two ways depending on **Mode**. In **Shape** mode it intercepts the collision shape of any block you flagged in **Avoid** and turns it into something solid you'll bump into instead of pass through — a full block for most hazards, or a short [4-pixel-tall cap](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleAvoidHazards.kt#L68-L87) for low hazards like pressure plates and magma blocks, so you're physically stopped at the edge. In **Input** mode it instead [simulates your next couple of movement ticks](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleAvoidHazards.kt#L110-L152) and, if your current input would walk you into a hazard, rewrites your direction keys to a safe alternative — letting you keep moving while steering clear rather than hitting an invisible wall.

Each hazard has its own [detection test](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleAvoidHazards.kt#L227-L262), and only the hazards you select in **Avoid** are acted on. Ladders are treated carefully — if you're already climbing, the module won't fight you; it only blocks transitions that would *newly* put you into a climb state.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | Shape | Shape, Input | How hazards are avoided. **Shape** makes flagged blocks solid so you collide with and stop at them; **Input** simulates upcoming ticks and redirects your movement keys to dodge hazards while still letting you move. |
| Avoid | Multi-Select | [Cacti, BerryBush, Fire, Cobwebs, Ladders, PressurePlates, MagmaBlocks, Lava, WitherRose, PowderSnow] | Cacti, BerryBush, Fire, Cobwebs, Ladders, PressurePlates, MagmaBlocks, Lava, WitherRose, PowderSnow | Which block hazards to avoid. Only the selected entries are detected and acted on; deselect any you'd rather walk into freely. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleAvoidHazards.kt)*
