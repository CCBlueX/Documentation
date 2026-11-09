## Parkour

Parkour automatically jumps at the very edge of a block, letting you chain block-to-block gaps without ever pressing the jump key manually. Instead of timing each leap yourself, the module detects when your next step would take you off the edge and fires a jump at the last possible moment — keeping your momentum and minimising the gap you need to clear.

With **Assist** enabled, Parkour also helps you land the jumps you run at. It picks the block across the gap you are heading for, jumps on the tick that lands best, turns the jump towards that block and steers in the air, then stops you on small landings. If there is no such block, it simply jumps at the edge.

This is most useful on parkour maps or any situation where you need to string together long sequences of jumps reliably. Because the jump triggers only when you are moving, on the ground, and not sneaking, normal walking and crouching are completely unaffected — you won't accidentally leap off ledges you meant to walk along. Combine it with [Speed](/docs/modules/movement/speed) or [NoJumpDelay](/docs/modules/movement/nojumpdelay) for faster parkour runs.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Assist | Toggleable Group | On | — | Assists jumps towards the block across the gap you are heading for. |
| Assist → MaxAngle | Decimal | 35 | 5..90 ° | How far from your movement direction a block may lie to be picked as the jump target. |
| Assist → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleParkour.kt)*
