## Backtrack

Backtrack shows you enemies where they were a moment ago, a little behind where they really are. This gives you more time to hit them. It only works shortly after you hit someone, and it lets go right away when the enemy's real spot is closer to you.

**Category:** Combat
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Range | Decimal Range | 1.0..3.0 | 0.0..10.0 | How close the enemy has to be, in blocks. |
| Delay | Integer Range | 100..150 | 0..1000 ms | How far behind the enemy is shown. |
| NextBacktrackDelay | Integer Range | 0..10 | 0..2000 ms | How long to wait before Backtrack works again. |
| TrackingBuffer | Integer | 500 | 0..2000 ms | How long to keep going after the enemy leaves Range. |
| Chance | Decimal | 50.0 | 0.0..100.0 % | How often Backtrack works when you hit. |
| PauseOnHurtTime | Toggleable Group | Off | | Pauses while the enemy was just hurt. |
| PauseOnHurtTime → HurtTime | Integer | 3 | 0..10 | How recently the enemy has to have been hurt for the pause, in ticks (20 per second). |
| TargetMode | Choice | Attack | Attack, Range | Who to use it on. Attack uses the enemy you hit. Range uses the closest enemy in Range. |
| LastAttackTimeToWork | Integer | 1000 | 0..5000 | Stops when you have not hit anyone for this long, in milliseconds. |
| Esp | Choice | Wireframe | Box, Model, Wireframe, None | How the enemy's real spot is drawn. None draws nothing. |
| Esp → [Box] → Color | Color | | | Color inside the box. |
| Esp → [Box] → OutlineColor | Color | | | Color of the box's edges. |
| Esp → [Model] → OutlineColor | Color | | | Color of the model's outline. |
| Esp → [Model] → LightPercent | Integer | 60 | 0..100 % | How bright the model is. |
| Esp → [Wireframe] → Color | Color | | | Color of the wireframe. |
| Esp → [Wireframe] → OutlineColor | Color | | | Color of the wireframe's edges. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/backtrack/ModuleBacktrack.kt)*
