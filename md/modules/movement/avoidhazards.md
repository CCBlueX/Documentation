## AvoidHazards

Prevents you from walking into blocks that might affect you negatively.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Choice | default: Shape | options: Shape, Input)
└── Avoid (Multi-Select | default: [Cacti, BerryBush, Fire, Cobwebs, Ladders, PressurePlates, MagmaBlocks, Lava, WitherRose, PowderSnow] | options: Cacti, BerryBush, Fire, Cobwebs, Ladders, PressurePlates, MagmaBlocks, Lava, WitherRose, PowderSnow)
```

### Settings Details

- **Mode** (Choice) — default: `Shape` — How hazards are avoided. **Shape** places invisible collision barriers on the hazardous blocks; **Input** instead blocks the movement input that would walk you into the hazard.
- **Avoid** (Multi-Select) — default: `Cacti`, `BerryBush`, `Fire`, `Cobwebs`, `Ladders`, `PressurePlates`, `MagmaBlocks`, `Lava`, `WitherRose`, `PowderSnow`; options: `Cacti`, `BerryBush`, `Fire`, `Cobwebs`, `Ladders`, `PressurePlates`, `MagmaBlocks`, `Lava`, `WitherRose`, `PowderSnow` — Selects which hazardous blocks to avoid walking into.

### Screenshots

*Screenshots for AvoidHazards will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleAvoidHazards.kt)*
