## HoleFiller

HoleFiller fills holes near enemies with obsidian, so they can't hide in them during crystal fights. A hole is a gap in bedrock or obsidian that keeps you safe from crystals.

By default it only fills a hole when an enemy is about to step in, and it leaves alone the hole you want to use yourself. It goes well with [CrystalAura](/docs/modules/combat/crystalaura) and [Surround](/docs/modules/world/surround).

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Features | Multi-Select | Smart, PreventSelfFill, CheckMovement | Smart, PreventSelfFill, OnlyWhenSelfInHole, CheckMovement, Only1x1 | Smart: only fill a hole when an enemy is about to get in. PreventSelfFill: don't fill the hole you want to use. OnlyWhenSelfInHole: only work while you stand in a hole. CheckMovement: only fill holes in the direction an enemy is walking (needs Smart). Only1x1: only fill holes one block wide. |
| Area | Integer | 2 | 1..5 | How many blocks around each player's feet to look for holes. |
| Filter | Choice | Whitelist | Whitelist, Blacklist | Whitelist: only use the blocks in the list. Blacklist: use any block except those. |
| Blocks | Registry List | Obsidian | | Blocks for the Filter. |
| Placing | Setting Group | | | See [Block Placer](/docs/modules/shared-settings/block-placer). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleHoleFiller.kt)*
