## ReverseStep

ReverseStep pulls you down ledges faster. When you walk off a block edge you land on the block below right away instead of slowly falling.

It does nothing when you jump on purpose. It also leaves you alone when the drop is taller than MaximumFallDistance or when water, cobwebs, powder snow, hay bales or slime blocks are below you. It goes well with [Step](/docs/modules/movement/step), which takes you up blocks.

Instant puts you on the ground at once. Strict moves you down at a fixed speed. Accelerator makes your normal fall faster.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Instant | Instant, Strict, Accelerator | How you are pulled down. |
| Mode → [Instant] → Ticks | Integer | 20 | 1..40 ticks | How far ahead it looks for the ground, in ticks (20 per second). |
| Mode → [Instant] → SimulateFalling | Toggle | false | | Tells the server about every step of the fall so it looks more normal. |
| Mode → [Strict] → Motion | Decimal | 1.0 | 0.1..5.0 | How fast you move down. |
| Mode → [Accelerator] → Factor | Decimal | 1.0 | 0.1..5.0 | How much faster you fall. Above 1.0 is faster, below 1.0 is slower. |
| MaximumFallDistance | Decimal | 1.0 | 1.0..50.0 | Highest drop in blocks it will pull you down. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/step/ModuleReverseStep.kt)*
