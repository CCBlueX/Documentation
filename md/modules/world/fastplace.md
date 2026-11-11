## FastPlace

FastPlace removes the short wait between placing blocks, so you can build as fast as you click or hold the button. It can also speed up throwing snowballs, eggs and ender pearls.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Cooldown | Integer Range | 0..0 | 0..4 ticks | Wait between uses, picked at random from the range (20 ticks per second). `0..0` is fastest. |
| ApplyTo | Multi-Select | Projectiles, Blocks | Projectiles, Blocks | What it speeds up: blocks, things you throw, or both. |
| StartDelay | Integer | 0 | 0..1000 ms | How long you must hold the button before it gets faster. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleFastPlace.kt)*
