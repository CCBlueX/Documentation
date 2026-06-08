## TargetStrafe

TargetStrafe automatically orbits your character around the enemy currently locked by [KillAura](/docs/modules/combat/killaura) or [Aimbot](/docs/modules/combat/aimbot), keeping you circling at a fixed distance. Continuously moving sideways around an opponent makes you much harder to hit while keeping you within melee reach — a significant edge in close-quarters PvP. If neither combat module has a lock, TargetStrafe falls back to its own built-in target selector.

Two movement modes control how the orbit is applied. **Motion** mode adjusts your velocity vector directly and includes a **Hypixel** sub-option that synchronises the strafe with [Speed](/docs/modules/movement/speed)'s low-hop timing so you don't bleed horizontal speed on Hypixel-style servers. **Input** mode redirects your directional keyboard input instead, making the strafe behave more like manual movement and potentially passing certain anti-cheat checks more cleanly. The **Requirements** setting gates activation — for example, requiring [KillAura](/docs/modules/combat/killaura) to be running and the jump key to be held — so the module only activates under the right conditions.

The **Planner** group validates each planned orbit step before your character moves there, checking for block collisions, nearby edges, and void drops. When a destination is blocked, the module reverses its strafe direction by default; enabling **AdaptiveRange** causes it to try progressively tighter orbit radii before reversing. The **Visuals** group renders a ring around the target showing the orbit path and a dot marking the next planned position — the dot turns red when that position is deemed unsafe.

**Category:** Movement  
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Motion | — | How the strafe movement is applied. **Motion** modifies movement velocity directly; **Input** redirects keyboard directional input. |
| Mode → [Motion] → Hypixel | Toggle | true | — | Synchronises strafe timing with [Speed](/docs/modules/movement/speed)'s Hypixel low-hop mode to avoid losing horizontal speed on Hypixel-style servers. |
| Range | Decimal | 0.5 | 0.0 – 8.0 | Target orbit radius — the distance from the enemy the module tries to maintain while circling. |
| FollowRange | Decimal | 3.0 | 0.0 – 10.0 | Maximum horizontal distance from the target at which strafing remains active. Beyond this the module pauses until you close in. |
| Requirements | Multi-Select | Space, Speed | — | Conditions that must all be satisfied for strafing to activate: **Space** (jump key held), **Speed** ([Speed](/docs/modules/movement/speed) active), **KillAura** ([KillAura](/docs/modules/combat/killaura) active), **Ground** (standing on the ground). |
| Planner | Toggleable Group | on | — | Plans and validates each orbit step before moving. Disabling skips all path-safety checks. |
| Planner → ControlDirection | Toggle | true | — | When on, pressing left or right overrides the automatic strafe direction. |
| Planner → Validation | Toggleable Group | on | — | Validates the next orbit position for safety before committing to movement. |
| Planner → Validation → EdgeCheck | Toggleable Group | on | — | Prevents strafing to positions where you would fall farther than the configured maximum height. |
| Planner → Validation → EdgeCheck → MaxFallHeight | Decimal | 1.2 | 0.1 – 4.0 | Maximum drop distance in blocks still considered safe when evaluating an orbit position. |
| Planner → Validation → VoidCheck | Toggleable Group | on | — | Prevents strafing to positions from which you would fall into the void. |
| Planner → Validation → VoidCheck → SafetyExpand | Decimal | 0.1 | 0.0 – 5.0 | Expands the void-detection boundary outward by this many blocks for an additional safety margin. |
| Planner → AdaptiveRange | Toggleable Group | off | — | When a destination is blocked, tries progressively closer orbit radii before reversing direction. |
| Planner → AdaptiveRange → MaxRange | Decimal | 4.0 | 1.0 – 5.0 | Largest orbit radius AdaptiveRange will attempt before giving up and reversing direction. |
| Planner → AdaptiveRange → RangeStep | Decimal | 0.5 | 0.1 – 1.0 | Amount by which the orbit radius increases with each adaptive step. |
| Visuals | Toggleable Group | on | — | Renders the orbit ring and next-step marker in the game world. |
| Visuals → Width | Decimal | 0.12 | 0.01 – 1.0 | Thickness of the orbit ring drawn around the target. |
| Visuals → HeightOffset | Decimal | 0.05 | -1.0 – 1.0 | Vertical offset of the ring and point marker relative to the target's position. |
| Visuals → OuterColor | Color | — | — | Fill colour for the outer edge of the orbit ring. |
| Visuals → InnerColor | Color | — | — | Fill colour for the inner edge of the orbit ring. |
| Visuals → OutlineColor | Color | — | — | Border colour of the orbit ring. |
| Visuals → ShowNextPoint | Toggle | true | — | Shows a dot at the next planned strafe position. |
| Visuals → PointRadius | Decimal | 0.18 | 0.05 – 1.0 | Radius of the next-position dot marker. |
| Visuals → PointColor | Color | — | — | Fill colour of the dot when the next position is valid. |
| Visuals → PointOutlineColor | Color | — | — | Border colour of the dot when the next position is valid. |
| Visuals → InvalidPointColor | Color | — | — | Fill colour of the dot when the next position is blocked or unsafe. |
| Visuals → InvalidPointOutlineColor | Color | — | — | Border colour of the dot when the next position is blocked or unsafe. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleTargetStrafe.kt)*
