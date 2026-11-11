## NoInterpolation

The game moves other players and mobs smoothly between their updates, so what you see is a little behind where they really are. NoInterpolation cuts this smoothing down, so they jump to their real place sooner. It only changes what you see.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ReduceBy | Integer | 3 | 1..3 | How much smoothing to remove. 3 removes the most. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleNoInterpolation.kt)*
