## ReverseStep

ReverseStep makes your character descend block edges faster than normal. In vanilla Minecraft, stepping down even a single block requires your character to fall naturally, which can feel sluggish. With this module enabled, you drop down to the next lower surface much more quickly, making traversal of staircase-like terrain, cliff edges, and descending paths noticeably smoother.

The module only activates when you are airborne and have not intentionally jumped — it will not interfere with normal jumps or movement. It also checks what lies below you before acting: if it detects water, cobwebs, powder snow, hay bales, or slime blocks in your fall path, or if the drop exceeds the configured **MaximumFallDistance**, it will hold back and let you fall normally to avoid unexpected outcomes. This makes it reasonably safe to leave enabled during general gameplay. If you also use [Step](/docs/modules/movement/step), the two modules complement each other — Step handles going up, ReverseStep handles coming down.

Three modes give you flexibility depending on which anti-cheat you are playing on. **Instant** simulates the entire fall in a single tick and teleports you to the landing position, with an optional packet-sending pass to make the movement look more legitimate to the server. **Strict** overrides your downward velocity with a fixed value each tick, producing a consistent descent speed. **Accelerator** multiplies your existing downward velocity by a configurable factor, speeding up the natural fall curve rather than replacing it outright.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Instant | Instant, Strict, Accelerator | Selects how the faster descent is applied. |
| Mode → [Instant] → Ticks | Integer | 20 | 1–40 ticks | Maximum number of ticks the fall simulation will run before giving up. |
| Mode → [Instant] → SimulateFalling | Toggle | false | — | When enabled, sends position packets for each simulated tick to the server, making the descent appear more gradual to anti-cheats. |
| Mode → [Strict] → Motion | Decimal | 1.0 | 0.1–5.0 | The fixed downward velocity applied each tick while descending. Higher values make you drop faster. |
| Mode → [Accelerator] → Factor | Decimal | 1.0 | 0.1–5.0 | Multiplier applied to your current downward velocity each tick. Values above 1.0 accelerate the fall; below 1.0 slow it. |
| MaximumFallDistance | Decimal | 1.0 | 1.0–50.0 | The maximum fall distance (in blocks) the module will act on. Drops deeper than this, or where no ground is detected within this range, are left unaffected. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/step/ModuleReverseStep.kt)*
