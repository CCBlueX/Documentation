## PotionFX

PotionFX draws custom visual effects for potions. Like other effect modules such as [JumpEffect](/docs/modules/render/jumpeffect) and [TotemEffect](/docs/modules/render/totemeffect), it is purely cosmetic and does not change how the potions themselves behave.

The module is split into three sections that are toggled independently: one for the effects on players, one for splash potions and one for lingering potions. Every effect is tinted with the colour of the potion it belongs to.

The lingering potion section draws a spinning texture flat on the ground over the area effect cloud, scaled to the cloud's own radius. A second spinning texture can be layered underneath it, and a glow can flash up while the cloud settles. Both textures are either one of the images bundled with LiquidBounce — **Dashed**, **Solid**, **Runes** or **Atlas** for the main layer, **Cracked**, **Neuron**, **Hexagon** or **Stardust** for the second — or an image file of your own.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| LingeringPotion | Toggleable Group | No | — | Draws an effect on the ground for the cloud left behind by a lingering potion. |
| LingeringPotion → MainEffect → ExtraRadius | Decimal | 0.375 | 0.0 – 10.0 | Added to the cloud's own radius when sizing the main texture. |
| LingeringPotion → MainEffect → RotationSpeed | Decimal | 1.0 | -10.0 – 10.0 | How fast the main texture spins. Negative values spin it the other way, 0 keeps it still. |
| LingeringPotion → Source | Mode Selector | Builtin | Builtin \| Custom | Where the main texture comes from: **Builtin** picks one of the images shipped with LiquidBounce, **Custom** uses an image file you provide. |
| LingeringPotion → SecondEffects → Flash | Toggleable Group | Yes | — | Flashes a glow that grows out of the cloud when it appears. |
| LingeringPotion → SecondEffects → Flash → AnimTime | Integer | 4 | 1 – 20 | How many ticks the glow takes to reach its full size. |
| LingeringPotion → SecondEffects → Flash → Radius | Decimal | 2.0 | 0.1 – 10.0 | Size of the glow at the end of its animation. |
| LingeringPotion → SecondEffects → Effect | Toggleable Group | No | — | Draws a second texture underneath the main one. |
| LingeringPotion → SecondEffects → Effect → RotationSpeed | Decimal | 1.0 | -10.0 – 10.0 | How fast the second texture spins. |
| LingeringPotion → SecondEffects → Effect → ExtraRadius | Decimal | 0.0 | 0.0 – 10.0 | Added to the size of the second texture, letting it stick out past the main one. |
| LingeringPotion → SecondEffects → Effect → Source | Mode Selector | Builtin | Builtin \| Custom | Where the second texture comes from. |
| LingeringPotion → CanBeCovered | Toggle | Yes | — | When enabled, blocks in the world can occlude the effect. When disabled, it always renders on top of geometry. |

---
*Last updated: 2026-08-27*
