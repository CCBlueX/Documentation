## NoPush

NoPush prevents external forces from altering your movement without your input. By default, it blocks pushes from other entities and liquids, keeping you firmly in place even when players walk into you or currents try to carry you along. This is especially useful in crowded PvP scenarios or when navigating rivers and ocean biomes where liquid flow would otherwise redirect your path.

The **PushBy** setting lets you choose exactly which push sources to suppress. **Entities** stops other players and mobs from nudging you on collision. **Blocks** prevents geometry (such as slime blocks or pistons) from displacing you. **FishingRod** stops the knockback applied when a fishing hook hits you. **Liquids** cancels the current-based drift in water and lava. The optional **Sinking** option goes a step further: while in water or lava, if you are not actively jumping or sneaking, downward movement caused by gravity in the fluid is cancelled — effectively letting you float in place vertically. Note that this option is not enabled by default.

NoPush pairs well with [Velocity](/docs/modules/combat/velocity) if you want comprehensive knockback resistance, since Velocity handles combat-sourced knockback that NoPush does not cover.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| PushBy | Multi-Select | Entities, Blocks, FishingRod, Liquids | Entities, Blocks, FishingRod, Liquids, Sinking | Select which push sources are blocked. **Entities** — other players/mobs; **Blocks** — piston/slime-block displacement; **FishingRod** — hook knockback; **Liquids** — fluid current drift; **Sinking** — prevents downward sinking in water/lava while not jumping or sneaking. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleNoPush.kt)*
