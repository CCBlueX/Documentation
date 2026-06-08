## FastPlace

FastPlace removes the short delay the game normally enforces between placing blocks (and, optionally, throwing projectiles), letting you build and spam items as fast as you can click or hold use. It's especially handy when bridging, walling off, or quickly stacking blocks under pressure.

By default it speeds up block placement only, with no extra cooldown of its own. If you'd rather rate-limit the effect to look more legitimate, raise **Cooldown** to add a small randomized tick delay back in. You can also include projectiles like snowballs, eggs, or ender pearls via **ApplyTo**, and use **StartDelay** to wait a moment after you begin holding use before the speed-up kicks in.

**Category:** World
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Cooldown | Integer Range | 0..0 | 0..4 | Randomized cooldown (in ticks) applied between uses. Leave at `0..0` for maximum speed, or raise it to throttle and randomize how fast items are used. |
| ApplyTo | Multi-Select | [Blocks] | Projectiles, Blocks | Which item types FastPlace affects. `Blocks` speeds up block placement, `Projectiles` speeds up throwable items like snowballs, eggs, and pearls. |
| StartDelay | Integer | 0 | 0..1000 | Delay (in ms) after you start holding the use key before the speed-up activates. `0` applies it immediately. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleFastPlace.kt)*
