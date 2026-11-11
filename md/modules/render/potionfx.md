## PotionFX

PotionFX draws spinning circles on the ground for potions: under players who have an effect, where a splash potion breaks, and over lingering potion clouds. Each one takes the color of its potion. It only changes what you see, not how potions work.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Players | Toggleable Group | on | | Draws a spinning circle under every player who has a potion effect. |
| Players → MainEffect → Radius | Decimal | 1.0 | 0.1 to 10.0 | Size of the circle. |
| Players → MainEffect → RotationSpeed | Decimal | 4.0 | -10.0 to 10.0 | How fast the circle spins. Negative values spin it the other way, 0 keeps it still. |
| Players → MainEffect → Source | Mode Selector | Builtin | Builtin, Custom | Where the texture comes from. **Builtin** uses an image that comes with LiquidBounce, **Custom** uses your own PNG or JPG file. |
| Players → MainEffect → Source → Builtin → Preset | Choice | Dashed | Dashed, Solid, Runes, Atlas | Which built-in image to use. |
| Players → MainEffect → Source → Custom → File | File | | | The PNG or JPG image to use. |
| Players → SecondEffect | Toggleable Group | off | | Draws a second image under the first one. |
| Players → SecondEffect → RotationSpeed | Decimal | 4.0 | -10.0 to 10.0 | How fast the second image spins. |
| Players → SecondEffect → ExtraRadius | Decimal | 0.0 | 0.0 to 10.0 | Makes the second image bigger than the first one. |
| Players → SecondEffect → Source | Mode Selector | Builtin | Builtin, Custom | Where the texture comes from. **Builtin** uses an image that comes with LiquidBounce, **Custom** uses your own PNG or JPG file. |
| Players → SecondEffect → Source → Builtin → Preset | Choice | Cracked | Cracked, Neuron, Hexagon, Stardust | Which built-in image to use. |
| Players → SecondEffect → Source → Custom → File | File | | | The PNG or JPG image to use. |
| Players → CanBeCovered | Toggle | true | | When on, blocks can hide the effect. When off, it is always drawn on top. |
| SplashPotion | Toggleable Group | on | | Draws a spinning circle on the ground where a splash potion breaks. |
| SplashPotion → MainEffect → Lifetime | Integer Range | 20..40 | 1..1000 | How long the effect stays, in ticks (20 per second). |
| SplashPotion → MainEffect → Radius | Decimal | 3.0 | 0.1 to 10.0 | Size of the circle. |
| SplashPotion → MainEffect → RotationSpeed | Decimal | 3.0 | -10.0 to 10.0 | How fast the circle spins. |
| SplashPotion → MainEffect → FadeStart | Decimal | 0.9 | 0.01 to 1.0 | How far into its life the effect starts to fade out. 0.9 means it fades during the last tenth. |
| SplashPotion → MainEffect → Source | Mode Selector | Builtin | Builtin, Custom | Where the texture comes from. **Builtin** uses an image that comes with LiquidBounce, **Custom** uses your own PNG or JPG file. |
| SplashPotion → MainEffect → Source → Builtin → Preset | Choice | Dashed | Dashed, Solid, Runes, Atlas | Which built-in image to use. |
| SplashPotion → MainEffect → Source → Custom → File | File | | | The PNG or JPG image to use. |
| SplashPotion → SecondEffects → Flash | Toggleable Group | on | | A glow that grows out of the spot where the potion broke. |
| SplashPotion → SecondEffects → Flash → AnimTime | Integer | 4 | 1 to 20 | How many ticks the glow takes to reach full size. |
| SplashPotion → SecondEffects → Flash → Radius | Decimal | 2.0 | 0.1 to 10.0 | Size of the glow at the end. |
| SplashPotion → SecondEffects → Effect | Toggleable Group | off | | Draws a second image under the first one. |
| SplashPotion → SecondEffects → Effect → AnimAcceleration | Decimal | 1.25 | 0.1 to 2.0 | How quickly the second image grows to full size. |
| SplashPotion → SecondEffects → Effect → RotationSpeed | Decimal | 3.0 | -10.0 to 10.0 | How fast the second image spins. |
| SplashPotion → SecondEffects → Effect → ExtraRadius | Decimal | 0.0 | 0.0 to 10.0 | Makes the second image bigger than the first one. |
| SplashPotion → SecondEffects → Effect → Source | Mode Selector | Builtin | Builtin, Custom | Where the texture comes from. **Builtin** uses an image that comes with LiquidBounce, **Custom** uses your own PNG or JPG file. |
| SplashPotion → SecondEffects → Effect → Source → Builtin → Preset | Choice | Cracked | Cracked, Neuron, Hexagon, Stardust | Which built-in image to use. |
| SplashPotion → SecondEffects → Effect → Source → Custom → File | File | | | The PNG or JPG image to use. |
| SplashPotion → CanBeCovered | Toggle | true | | When on, blocks can hide the effect. When off, it is always drawn on top. |
| LingeringPotion | Toggleable Group | off | | Draws a spinning circle over the cloud a lingering potion leaves behind, sized to the cloud. |
| LingeringPotion → MainEffect → ExtraRadius | Decimal | 0.375 | 0.0 to 10.0 | Added to the cloud's size. |
| LingeringPotion → MainEffect → RotationSpeed | Decimal | 1.0 | -10.0 to 10.0 | How fast the circle spins. |
| LingeringPotion → MainEffect → Source | Mode Selector | Builtin | Builtin, Custom | Where the texture comes from. **Builtin** uses an image that comes with LiquidBounce, **Custom** uses your own PNG or JPG file. |
| LingeringPotion → MainEffect → Source → Builtin → Preset | Choice | Dashed | Dashed, Solid, Runes, Atlas | Which built-in image to use. |
| LingeringPotion → MainEffect → Source → Custom → File | File | | | The PNG or JPG image to use. |
| LingeringPotion → SecondEffects → Flash | Toggleable Group | on | | A glow that grows out of the cloud when it appears. |
| LingeringPotion → SecondEffects → Flash → AnimTime | Integer | 4 | 1 to 20 | How many ticks the glow takes to reach full size. |
| LingeringPotion → SecondEffects → Flash → Radius | Decimal | 2.0 | 0.1 to 10.0 | Size of the glow at the end. |
| LingeringPotion → SecondEffects → Effect | Toggleable Group | off | | Draws a second image under the first one. |
| LingeringPotion → SecondEffects → Effect → RotationSpeed | Decimal | 1.0 | -10.0 to 10.0 | How fast the second image spins. |
| LingeringPotion → SecondEffects → Effect → ExtraRadius | Decimal | 0.0 | 0.0 to 10.0 | Makes the second image bigger than the first one. |
| LingeringPotion → SecondEffects → Effect → Source | Mode Selector | Builtin | Builtin, Custom | Where the texture comes from. **Builtin** uses an image that comes with LiquidBounce, **Custom** uses your own PNG or JPG file. |
| LingeringPotion → SecondEffects → Effect → Source → Builtin → Preset | Choice | Cracked | Cracked, Neuron, Hexagon, Stardust | Which built-in image to use. |
| LingeringPotion → SecondEffects → Effect → Source → Custom → File | File | | | The PNG or JPG image to use. |
| LingeringPotion → CanBeCovered | Toggle | true | | When on, blocks can hide the effect. When off, it is always drawn on top. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/potionfx/ModulePotionFX.kt)*
