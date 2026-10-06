## Eagle

Eagle automatically sneaks whenever you reach the edge of the block you're standing on, so you don't walk off and fall. This is the classic "legit" bridging trick: you can move forward at full pace while the module taps sneak for you right as you near each ledge, letting you bridge out over gaps quickly and safely without manually holding the sneak key. Because it only mimics normal sneaking, it's one of the least suspicious ways to build out fast.

It's a good companion to manual bridging when you don't want the more aggressive automation of [Scaffold](/docs/modules/world/scaffold). Use `EdgeDistance` to tune how close to the edge you get before it sneaks — smaller values let you reach further out (more speed, more risk), larger values keep you well back from the drop.

The `Conditional` group lets you restrict when Eagle is allowed to take over, so it only kicks in under the situations you choose (for example, only while on the ground or only while holding blocks). When `Sneak` is one of the active conditions, Eagle can take control of your sneak key for you.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| EdgeDistance | Decimal Range | 0.4..0.6 | 0.01..1.3 | How close to the edge of a block you get before Eagle sneaks. Lower values let you stand further out over the edge before sneaking; higher values keep you back from the drop. A fresh random distance within this range is picked each time to vary the behavior. |
| Conditional | Toggleable Group | on | — | Restricts when Eagle is allowed to activate. Turn off to let Eagle sneak at every edge regardless of conditions. |
| Conditional → Conditions | Multi-Select | [OnGround] | options: [Left, Right, Forwards, Backwards, HoldingBlocks, OnGround, Sneak] | The conditions that must all be met for Eagle to act — based on movement direction, whether you're holding placeable blocks, whether you're on the ground, and whether you're sneaking. Including Sneak lets Eagle take over control of your sneak key. |
| Conditional → Pitch | Decimal Range | -90.0..90.0 | -90.0..90.0 | The vertical look (pitch) range you must be looking within for Eagle to act. The default covers all angles; narrow it to only sneak while looking down, for example. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleEagle.kt)*
