## Spider

Spider lets you climb straight up walls like a spider. Walk into a wall and you move up instead of standing still. It is handy for getting onto high places when you have no ladder.

Vanilla works in singleplayer and on servers without an anti-cheat. Polar-2025-03-29 is made for the Polar anti-cheat and Vulcan-2.8.8 for Vulcan. Turn on [NoFall](/docs/modules/player/nofall) too, in case you fall off the wall.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Vanilla | Vanilla, Polar-2025-03-29, Vulcan-2.8.8 | How you climb. Pick the one that fits the server's anti-cheat. |
| Mode → [Vanilla] → Motion | Decimal | 0.3 | 0.05..0.8 | How fast you climb. Higher is faster but easier to notice. |
| Mode → [Polar-2025-03-29] → JumpHeight | Decimal | 0.55 | 0.42..0.6 | How high each climbing jump goes. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/spider/ModuleSpider.kt)*
