## HoleFiller

HoleFiller automatically places blocks into nearby holes so opponents can't dive into a safe spot to dodge your crystals. In crystal PvP, a "hole" is a tight gap in bedrock or obsidian that protects whoever stands in it — HoleFiller watches for those gaps around enemies and packs them with obsidian (or whatever block you choose) before the enemy can reach safety. It's a strong companion to [CrystalAura](/docs/modules/combat/crystalaura), and works well alongside [Surround](/docs/modules/world/surround) for keeping yourself protected while you trap others.

By default it runs in **Smart** mode, meaning it only fills a hole when an enemy is actually about to step into it, rather than wastefully blocking every gap on the map. It also tries to avoid sealing the hole you yourself want to drop into, and it can check an enemy's movement direction so it only commits blocks to spots they're genuinely heading toward. You can widen or narrow how far around feet it scans, restrict it to only the tiny 1×1 holes, or have it act only while you're standing in a hole yourself.

All the actual block placement — rotations, swing, timing, support requirements and so on — is handled by the shared [Block Placer](/docs/modules/shared-settings/block-placer) group, so you can tune how aggressively and how legitimately the blocks go down.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Features | Multi-Select | [Smart, PreventSelfFill, CheckMovement] | Smart, PreventSelfFill, OnlyWhenSelfInHole, CheckMovement, Only1x1 | Toggles for how holes are chosen. **Smart** only fills holes when an enemy is about to enter one (otherwise every hole in range is filled). **PreventSelfFill** stops it from blocking the hole you want to drop into. **OnlyWhenSelfInHole** makes it act only while you are standing in a hole. **CheckMovement** ignores holes more than 30° away from an enemy's movement direction (only applies with Smart). **Only1x1** restricts filling to single-block holes, ignoring larger 2×1 and 2×2 ones. |
| Area | Integer | 2 | 1..5 | How far around each entity's feet (in blocks) is scanned for holes to fill. Larger values react to holes further from the target. |
| Filter | Choice | Whitelist | Whitelist, Blacklist | How the block list is applied — **Whitelist** only fills using the listed blocks, **Blacklist** uses any block except the listed ones. |
| Blocks | Registry List | — | — | The blocks used to fill holes (and, with Blacklist, the blocks to avoid). Defaults to obsidian. |
| Placing | Setting Group | — | — | See [Shared: Block Placer](/docs/modules/shared-settings/block-placer). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleHoleFiller.kt)*
