## NoSlow

NoSlow removes the movement penalties that Minecraft normally applies while you interact with items or stand on certain blocks. Each source of slowdown has its own switch, so you can keep full walking and strafing speed while eating, drinking, blocking with a shield, drawing a bow, sneaking, or crossing sticky terrain.

The item-based groups (Blocking, Consume, Bow, Bundle) let you fine-tune how much of your speed is kept on the forward and sideways axes, and most of them offer anti-cheat bypass methods named after the anti-cheat and version they were built for (Grim, Intave, AAC). Pick the method that matches the server you play on; the default `None` simply applies the speed multipliers client-side. The Blocking group also includes a Blink method that queues your movement packets the same way [Blink](/docs/modules/player/blink) does.

The block and environment groups (Soulsand, SlimeBlock, HoneyBlock, PowderSnow, Fluid) override the speed those blocks would normally take away, while Sneaking softens the crouch penalty and Slowness reduces the Slowness potion effect. Note that mining/breaking slowdown is handled by the separate [NoSlowBreak](/docs/modules/world/noslowbreak) module.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Blocking | Toggleable Group | on | — | Cancels the slowdown while blocking with a shield (or a sword via protocol translation). |
| Blocking → Forward | Decimal | 1.0 | 0.0–1.0 | Fraction of forward/back speed kept while blocking (1.0 = full speed). |
| Blocking → Sideways | Decimal | 1.0 | 0.0–1.0 | Fraction of strafing speed kept while blocking. |
| Blocking → OnlySlowOnServerSide | Toggle | false | — | When on, only cancels slowdown for blocking that exists purely server-side, leaving normal client-side blocking slowed. |
| Blocking → Choice | Mode Selector | None | None, Reuse, Switch, Blink, Interact, Grim2360, Grim2364-1.8, Grim2371, InvalidHand, Intave14 | Anti-cheat bypass method used for blocking slowdown. |
| Blocking → Choice → [Reuse] → Timing | Choice | Post | PreAndPost, Pre, Post | When the release-and-reuse packets are sent each tick. |
| Blocking → Choice → [Switch] → Timing | Choice | Post | PreAndPost, Pre, Post | When the slot-switch packets are sent each tick. |
| Consume | Toggleable Group | off | — | Cancels the slowdown while eating or drinking. |
| Consume → Forward | Decimal | 1.0 | 0.0–1.0 | Fraction of forward/back speed kept while consuming. |
| Consume → Sideways | Decimal | 1.0 | 0.0–1.0 | Fraction of strafing speed kept while consuming. |
| Consume → NoBlockInteract | Toggleable Group | off | — | Cancels block interactions while consuming to avoid flagging on some anti-cheats. |
| Consume → Mode | Mode Selector | None | None, Grim2360, Grim2364-1.8, InvalidHand, Grim2371, Jump, Intave14, Release | Anti-cheat bypass method used for consume slowdown. |
| Consume → Mode → [Intave14] → Mode | Choice | Release | Release, New | Variant of the Intave 14 bypass to use. |
| Bow | Toggleable Group | off | — | Cancels the slowdown while charging a bow, crossbow, or trident. |
| Bow → Forward | Decimal | 0.75 | 0.0–1.0 | Fraction of forward/back speed kept while drawing. |
| Bow → Sideways | Decimal | 0.75 | 0.0–1.0 | Fraction of strafing speed kept while drawing. |
| Bow → Choice | Mode Selector | None | None, Grim2360, Grim2364-1.8, Grim2371, InvalidHand | Anti-cheat bypass method used for bow slowdown. |
| Bow → NoBlockInteract | Toggleable Group | on | — | Cancels block interactions while drawing to avoid flagging on some anti-cheats. |
| Bundle | Toggleable Group | off | — | Cancels the slowdown while using a bundle. |
| Bundle → Forward | Decimal | 1.0 | 0.0–1.0 | Fraction of forward/back speed kept while using a bundle. |
| Bundle → Sideways | Decimal | 1.0 | 0.0–1.0 | Fraction of strafing speed kept while using a bundle. |
| Sneaking | Toggleable Group | off | — | Reduces or removes the movement penalty while sneaking. |
| Sneaking → MinMultiplier | Decimal | 1.0 | 0.3–1.0 | Minimum fraction of speed kept while sneaking (1.0 = no slowdown). |
| Sneaking → Mode | Mode Selector | None | None, Switch, AAC5 | Anti-cheat bypass method (only works on servers older than 1.21.6). |
| Sneaking → Mode → [Switch] → Timing | Choice | PreAndPost | PreAndPost, Pre, Post | When the sneak packets are sent each tick. |
| Sneaking → Mode → [AAC5] → Timing | Choice | PreAndPost | PreAndPost, Pre, Post | When the sneak packets are sent each tick. |
| Soulsand | Toggleable Group | off | — | Overrides the speed penalty when walking on soul sand. |
| Soulsand → Multiplier | Decimal | 1.0 | 0.4–2.0 | Speed multiplier on soul sand (1.0 = normal speed, higher = faster). |
| SlimeBlock | Toggleable Group | off | — | Overrides the speed penalty and bounce when on slime blocks. |
| SlimeBlock → Multiplier | Decimal | 1.0 | 0.4–2.0 | Speed multiplier on slime blocks (1.0 = normal speed, higher = faster). |
| HoneyBlock | Toggleable Group | off | — | Overrides the speed penalty when on honey blocks. |
| HoneyBlock → Multiplier | Decimal | 1.0 | 0.4–2.0 | Speed multiplier on honey blocks (1.0 = normal speed, higher = faster). |
| PowderSnow | Toggleable Group | off | — | Overrides the speed penalty when walking through powder snow. |
| PowderSnow → Multiplier | Decimal | 1.0 | 0.4–2.0 | Speed multiplier in powder snow (1.0 = normal speed, higher = faster). |
| Fluid | Toggleable Group | off | — | Stops water and lava currents from pushing or slowing you. |
| Fluid → Collision | Toggle | false | — | Whether to keep fluid collision. When off, fluids no longer affect your movement. |
| Slowness | Toggleable Group | off | — | Reduces the effect of the Slowness potion. |
| Slowness → PerLevelMultiplier | Decimal | 0.0 | 0.0–0.15 | How much slowdown remains per Slowness level (0.0 fully cancels it; vanilla is 0.15). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/noslow/ModuleNoSlow.kt)*
