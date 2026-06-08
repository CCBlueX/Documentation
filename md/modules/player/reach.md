## Reach

Reach extends how far your character can interact with the world, letting you hit entities and break or place blocks from a greater distance than normal. This is useful in PvP situations where landing hits just outside standard range gives you an edge, as well as in building or mining scenarios where you want to interact with blocks without repositioning.

The module splits reach into two independent controls: entity reach (for attacking or interacting with mobs and players) and block reach (for clicking on blocks). You can tune each independently — for example, boosting entity reach for combat while leaving block range at its default, or increasing both when building at a distance. Pair this with [KillAura](/docs/modules/combat/killaura) or [AutoClicker](/docs/modules/combat/autoclicker) to take full advantage of the extended entity range in combat.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Entity | Setting Group | — | — | See [Shared: Range](/docs/modules/shared-settings/range). |
| BlockRangeIncrease | Decimal | 0.5 | 0.0 – 64.0 | How many extra blocks are added to your block interaction reach. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleReach.kt)*
