## Spider

Spider lets you climb vertical walls by negating gravity whenever you are pressed against a block. Instead of sliding back down when you walk into a wall, you will continuously move upward, just like a spider mob. This is useful for scaling fortress walls, reaching high platforms quickly, or escaping dangerous situations where ladders or scaffolding are unavailable.

Three modes are available to fit different server environments. **Vanilla** is a straightforward, unobfuscated approach that works on unprotected servers or in singleplayer. **Polar-29.03.2025** is tuned for servers running the Polar anti-cheat (as of late March 2025) — it subtly shrinks block collision shapes and adjusts jump height to climb without triggering flags. **Vulcan288** targets the Vulcan 2.8.8 anti-cheat; it uses a timed movement sequence to work around detection. Pair Spider with [NoFall](/docs/modules/player/nofall) so you do not take damage if you accidentally stop touching the wall mid-climb.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Vanilla | Vanilla, Polar-29.03.2025, Vulcan288 | Selects the wall-climbing behaviour. Choose the mode that matches your target server's anti-cheat. |
| Mode → [Vanilla] → Motion | Decimal | 0.3 | 0.05–0.8 | Upward velocity applied each tick while you are touching a wall. Higher values climb faster but may look more suspicious. |
| Mode → [Polar-29.03.2025] → JumpHeight | Decimal | 0.55 | 0.42–0.6 | Jump motion used when climbing against a wall in Polar mode. Lower values hug the block collision shape more conservatively. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/spider/ModuleSpider.kt)*
