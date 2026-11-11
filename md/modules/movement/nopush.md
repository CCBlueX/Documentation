## NoPush

NoPush stops things from pushing you around. Players and mobs can't shove you, and water won't carry you away. It does not stop knockback from hits; use [Velocity](/docs/modules/combat/velocity) for that.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| PushBy | Multi-Select | Entities, Liquids | Entities, Blocks, FishingRod, Liquids, Sinking | What can no longer push you. Entities: players and mobs walking into you. Blocks: being pushed out of blocks. FishingRod: getting pulled by a fishing hook. Liquids: flowing water. Sinking: you stop sinking in water and lava unless you hold Jump or Sneak. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleNoPush.kt)*
