## Clip

Clip teleports you through walls, floors and ceilings. Strict anti-cheats often catch it.

Fancy mode works while you walk into a wall, or hold jump or sneak under a ceiling or over a floor. It finds the nearest free spot on the other side and moves you there. Arrows next to your crosshair show if you can clip up or down. It does nothing while [Fly](/docs/modules/movement/fly) is on. Old mode teleports you a fixed distance once when you turn it on, then turns itself off.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Choice | Mode Selector | Fancy | Fancy, Old | How clipping works. |
| Choice → [Fancy] → Horizontal | Integer | 0 | 0..6 | How many blocks you can clip forward through a wall. |
| Choice → [Fancy] → Vertical | Integer | 5 | 0..10 | How many blocks you can clip up or down. |
| Choice → [Fancy] → AllowedLiquids | Multi-Select | None | Water, Lava | Liquids you may land in. Without these, it only moves you into air. |
| Choice → [Fancy] → RequiresStandOn | Toggle | true |  | Only clip to spots where you can stand. |
| Choice → [Old] → Horizontal | Decimal | 0.0 | -10.0..10.0 | Blocks to teleport forward, in the direction you look. |
| Choice → [Old] → Vertical | Decimal | 5.0 | -10.0..10.0 | Blocks to teleport up. Negative goes down. |
| Choice → [Old] → ResetVelocity | Toggle | true |  | Stop your movement after the teleport. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/exploit/ModuleClip.kt)*
