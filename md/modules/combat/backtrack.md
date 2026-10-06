## Backtrack

Backtrack holds back the packets the server sends you about an enemy, so the position you see and attack lags slightly behind where the enemy actually is. This gives you a larger, more forgiving window to land hits — you're effectively swinging at a recent "ghost" of the target while the client decides when to catch up. It builds on the client's Blink/packet-queue system, queuing incoming position updates and releasing them after a short, randomized delay; see [the incoming packet handler](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/backtrack/ModuleBacktrack.kt#L106-L174) and [the delayed flush logic](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/backtrack/ModuleBacktrack.kt#L193-L218).

Use it in close-range combat when you want extra leniency on your hits. It only engages under a set of conditions checked in [`shouldBacktrack`](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/backtrack/ModuleBacktrack.kt#L288-L303): the target must be within **Range**, valid to attack, you must have attacked recently (**LastAttackTimeToWork**), the random roll must pass **Chance**, and the cooldown (**NextBacktrackDelay**) must have elapsed. To keep you fair to yourself, the module automatically flushes its queue and snaps to the enemy's real position whenever that position is actually closer to you than the lagged one, so you never lose a hit you could otherwise make.

You can drive it off the entity you click (**TargetMode: Attack**) or the nearest enemy in range (**TargetMode: Range**), and visualize the tracked, lagged position with the **Esp** renderer.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal Range | 1.0..3.0 | 0.0..10.0 | Distance window (in blocks) the target must be in for backtracking to activate. |
| Delay | Integer Range | 100..150 | 0..1000 ms | How long incoming packets about the target are held back. A value in this range is rolled each cycle and packets are flushed once older than it. |
| NextBacktrackDelay | Integer Range | 0..10 | 0..2000 ms | Cooldown applied after a backtrack ends before the module will start backtracking again. A random value in this range is used each time. |
| TrackingBuffer | Integer | 500 | 0..2000 ms | Grace period to keep backtracking a target after it leaves Range, before giving up. |
| Chance | Decimal | 50.0 | 0.0..100.0 % | Probability that backtracking engages, re-rolled on each attack. |
| PauseOnHurtTime | Toggleable Group | off | — | When enabled, temporarily pauses backtracking while the target is in its hurt-animation state. |
| PauseOnHurtTime → HurtTime | Integer | 3 | 0..10 | Minimum remaining hurt ticks on the target required to trigger the pause. |
| TargetMode | Choice | Attack | Attack, Range | How a target is chosen: **Attack** backtracks the entity you hit; **Range** backtracks the nearest enemy within Range each tick. |
| LastAttackTimeToWork | Integer | 1000 | 0..5000 | Backtrack only stays active if you attacked within this many milliseconds; otherwise it stops. |
| Esp | Mode Selector | Wireframe | Box, Model, Wireframe, None | How the target's tracked (lagged) position is rendered. **None** disables the visual. |
| Esp → [Box] → Color | Color | — | — | Fill color of the box drawn at the tracked position. |
| Esp → [Box] → OutlineColor | Color | — | — | Outline color of the box drawn at the tracked position. |
| Esp → [Model] → OutlineColor | Color | — | — | Outline color of the rendered entity model at the tracked position. |
| Esp → [Model] → LightPercent | Integer | 60 | 0..100 % | Brightness of the rendered model at the tracked position. |
| Esp → [Wireframe] → Color | Color | — | — | Fill/line color of the wireframe drawn at the tracked position. |
| Esp → [Wireframe] → OutlineColor | Color | — | — | Outline color of the wireframe drawn at the tracked position. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/backtrack/ModuleBacktrack.kt)*
