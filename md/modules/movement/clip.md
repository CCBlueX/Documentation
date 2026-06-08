## Clip

Clip lets you slip through solid blocks by teleporting yourself a set distance in the direction you're moving. It's handy for getting past walls, floors, or ceilings that would normally stop you, and it works by snapping your position forward rather than walking through gradually.

It offers two modes. **Fancy** is the smarter, continuous option: while you press into a wall (or hold jump/sneak against a ceiling or floor), it scans for the nearest open space on the other side and clips you there, repeating as long as you keep moving. It also shows ▲/▼ markers next to your crosshair to indicate which vertical clips are currently available, and it stays out of the way while [Fly](/docs/modules/movement/fly) is active. **Old** is a one-shot teleport: the moment you enable the module it jumps you a fixed horizontal and vertical distance based on where you're facing, then turns itself back off.

Because clipping moves you in ways the server doesn't expect, results depend heavily on the server's anti-cheat — expect it to fail or flag you on stricter setups.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Choice | Mode Selector | Fancy | Fancy, Old | Chooses how clipping works: continuous wall-scanning (Fancy) or a single fixed teleport (Old). |
| Choice → [Fancy] → Horizontal | Integer | 5 | 0..6 | Maximum number of blocks to clip forward when pushing into a wall. |
| Choice → [Fancy] → Vertical | Integer | 5 | 0..6 | Maximum number of blocks to clip up or down when holding jump or sneak. |
| Choice → [Fancy] → RequiresStandOn | Toggle | true | — | Only clips to spots where there's solid ground to stand on, avoiding teleporting into mid-air. |
| Choice → [Old] → Horizontal | Decimal | 0.0 | -10.0..10.0 | Distance to teleport forward (relative to your facing) when the module is enabled. |
| Choice → [Old] → Vertical | Decimal | 5.0 | -10.0..10.0 | Distance to teleport up (or down, if negative) when the module is enabled. |
| Choice → [Old] → ResetVelocity | Toggle | true | — | Cancels your momentum after the teleport so you don't keep sliding. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/exploit/ModuleClip.kt)*
