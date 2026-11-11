## FastBreak

FastBreak lets you break blocks faster. When a block is almost broken, it breaks it right away, and there is no pause before you start on the next block.

Use [AutoTool](/docs/modules/world/autotool) to always hold the best tool, and [NoSlowBreak](/docs/modules/world/noslowbreak) to mine fast in water or in the air.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| BreakDamage | Decimal | 0.8 | 0.1..1.0 | How far the block must be broken before it breaks right away. Lower is faster. |
| OnlyTool | Toggle | false | | Only works while you hold a mining tool. |
| Mode | Mode Selector | None | None, Grim-2.3.48 | Grim-2.3.48 helps against the Grim anticheat. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleFastBreak.kt)*
