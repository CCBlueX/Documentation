## TargetStrafe

TargetStrafe makes you run in circles around the enemy you are fighting. Moving around them all the time makes you harder to hit while you stay close enough to hit them. It follows the target of [KillAura](/docs/modules/combat/killaura) or [Aimbot](/docs/modules/combat/aimbot), or picks its own target if neither has one.

Motion mode changes your movement directly. Input mode presses the movement keys for you, which looks more like a real player. With Requirements you can make it work only when, for example, you hold jump or [Speed](/docs/modules/movement/speed) is on. When nothing is picked, it always works.

The Planner checks each next spot before you move there, so you do not run into walls, off edges or into the void. If the spot is not safe, you turn around and circle the other way. The Visuals group draws a ring around the target and a dot where you go next. The dot turns red when that spot is not safe.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Motion | Motion, Input | Motion changes your movement directly. Input presses the movement keys for you. |
| Mode → [Motion] → Hypixel | Toggle | false | | Matches the circling to [Speed](/docs/modules/movement/speed)'s Hypixel hops so you keep your speed. |
| Range | Decimal | 2.95 | 0.0..8.0 | How far from the target you circle. |
| FollowRange | Decimal | 4.0 | 0.0..10.0 | Only circles when the target is closer than this. It is never smaller than Range. |
| Requirements | Multi-Select | none | Space, Speed, KillAura, Ground | Everything picked here must be true: Space (jump key held), Speed (Speed is on), KillAura (KillAura is on), Ground (you stand on the ground). |
| Planner | Toggleable Group | on | | Checks each next spot before moving there. |
| Planner → ControlDirection | Toggle | true | | Pressing left or right picks which way you circle. |
| Planner → Validation | Toggleable Group | on | | Makes sure the next spot is safe. |
| Planner → Validation → EdgeCheck | Toggleable Group | on | | Avoids spots where you would fall too far. |
| Planner → Validation → EdgeCheck → MaxFallHeight | Decimal | 1.2 | 0.1..4.0 | Biggest drop in blocks that still counts as safe. |
| Planner → Validation → VoidCheck | Toggleable Group | on | | Avoids spots where you would fall into the void. |
| Planner → Validation → VoidCheck → SafetyExpand | Decimal | 0.1 | 0.0..5.0 | Extra space in blocks to keep from the void. |
| Planner → AdaptiveRange | Toggleable Group | off | | When a spot is blocked, tries other distances before turning around. |
| Planner → AdaptiveRange → MaxRange | Decimal | 4.0 | 1.0..5.0 | Largest distance it tries. |
| Planner → AdaptiveRange → RangeStep | Decimal | 0.5 | 0.1..1.0 | How much the distance changes with each try. |
| Visuals | Toggleable Group | on | | Draws the ring and the next-spot dot. |
| Visuals → Width | Decimal | 0.12 | 0.01..1.0 | How thick the ring is. |
| Visuals → HeightOffset | Decimal | 0.05 | -1.0..1.0 | Moves the ring and dot up or down. |
| Visuals → OuterColor | Color | | | Color of the outer edge of the ring. |
| Visuals → InnerColor | Color | | | Color of the inner edge of the ring. |
| Visuals → ShowNextPoint | Toggle | true | | Shows a dot where you move next. |
| Visuals → PointRadius | Decimal | 0.18 | 0.05..1.0 | Size of the dot. |
| Visuals → PointColor | Color | | | Dot color when the spot is safe. |
| Visuals → InvalidPointColor | Color | | | Dot color when the spot is not safe. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleTargetStrafe.kt)*
