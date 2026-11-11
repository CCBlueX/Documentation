## AvoidHazards

AvoidHazards keeps you from walking into blocks that hurt or trap you, like cactus, fire, lava and cobwebs. Turn it on when you move fast and don't want to run into one by accident.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Shape | Shape, Input | Shape: the blocks you picked turn solid, so you bump into them and stop. Input: the client looks a little ahead and changes your movement keys so you walk around them. |
| Avoid | Multi-Select | All | Cacti, BerryBush, Fire, Cobwebs, Ladders, PressurePlates, MagmaBlocks, Lava, WitherRose, PowderSnow | Which blocks to avoid. For ladders, it only stops you from starting to climb. If you already climb, it leaves you alone. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleAvoidHazards.kt)*
