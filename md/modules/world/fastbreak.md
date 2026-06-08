## FastBreak

FastBreak lets you mine and break blocks faster than vanilla normally allows. While it's enabled, the time it takes for a block to break is shortened, so you can clear terrain, harvest, or dig through obstacles much more quickly.

You can fine-tune how aggressive the speed-up is with **BreakDamage**, and restrict it to only kick in while you're holding a proper mining tool with **OnlyTool** — handy if you don't want it interfering when you punch blocks by hand. The **Mode** option chooses how FastBreak behaves on the network side, which can help it stay under the radar on servers running certain anti-cheats. If you want to keep digging speed up while moving or jumping, pair it with [NoSlowBreak](/docs/modules/world/noslowbreak), and let [AutoTool](/docs/modules/world/autotool) handle swapping to the best tool automatically.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| BreakDamage | Decimal | 0.308 | 0.1..1.0 | How far a block's break progress must reach before FastBreak finishes it instantly. Lower values break blocks sooner (more aggressive); higher values wait until the block is nearly broken on its own. |
| OnlyTool | Toggle | false | — | When enabled, FastBreak only works while you're holding an appropriate mining tool, leaving bare-hand and other items at normal speed. |
| Mode | Mode Selector | AbortAnother | None, AbortAnother | Chooses how FastBreak operates. **None** simply applies the faster breaking. **AbortAnother** adds extra block-action packets designed to slip past certain anti-cheats while still breaking quickly. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleFastBreak.kt)*
