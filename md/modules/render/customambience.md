## CustomAmbience

CustomAmbience changes how the world looks on your screen: weather, time of day, fog, light and sky color. Other players still see the real weather and time. Set Weather or Time to NoChange to keep the real one.

You can use it to clear fog, lock a time of day you like, or add floating particles around you. It goes well with [FullBright](/docs/modules/render/fullbright) and [AntiBlind](/docs/modules/render/antiblind).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Weather | Choice | Snowy | NoChange, Sunny, Rainy, Snowy, Thunder | The weather you see. |
| Time | Choice | Night | NoChange, Dawn, Day, Noon, Dusk, Night, MidNight | The time of day you see. |
| ModifyPrecipitation | Toggleable Group | On | | Changes how rain and snow look. |
| ModifyPrecipitation → Gradient | Decimal | 0.7 | 0.1..1.0 | How thick the rain or snow is. |
| Fog | Toggleable Group | On | | Changes the fog. |
| Fog → DisableWorldFog | Toggle | false | | Removes the fog. |
| Fog → FogColorOverride | Toggleable Group | On | | Gives the fog your own color. |
| Fog → FogColorOverride → Color | Color | Light blue | | Fog color. |
| Fog → BackgroundColor | Color | Light blue | | Color far away, where the fog ends. |
| Fog → Environmental | Decimal Range | 5.0..40.0 | -16.0..2048.0 | Where fog from things like water or blindness starts and ends. |
| Fog → RenderDistance | Decimal Range | 230.0..256.0 | 0.0..1024.0 | Where fog at the edge of your render distance starts and ends. |
| Fog → SkyEnd | Decimal | 40.0 | 0.0..1024.0 | Where the sky fog ends. |
| Fog → CloudEnd | Decimal | 40.0 | 0.0..4096.0 | Where the cloud fog ends. |
| CustomLightmap | Toggleable Group | On | | Changes the light colors. |
| CustomLightmap → Mode | Mode Selector | SingleColor | SingleColor, Custom | SingleColor lights everything in one color. Custom tints single kinds of light. |
| CustomLightmap → Mode → [SingleColor] → Color | Color | Light blue | | The light color. |
| CustomLightmap → Mode → [Custom] → BlockLightTint | Color | Off (clear) | | Tint for light from torches and other blocks. |
| CustomLightmap → Mode → [Custom] → SkyLightColor | Color | Off (clear) | | Color of light from the sky. |
| CustomLightmap → Mode → [Custom] → AmbientColor | Color | Off (clear) | | Base color of all light. |
| CustomLightmap → Mode → [Custom] → NightVisionColor | Color | Off (clear) | | Light color with Night Vision. |
| SkyColor | Toggleable Group | Off | | Paints the sky in one color. |
| SkyColor → Color | Color | Light blue | | Sky color. |
| WorldParticles | Toggleable Group | Off | | Shows floating particles around you. |
| WorldParticles → Mode | Mode Selector | Simple | Simple | Particle style. |
| WorldParticles → [Simple] → Radius | Integer Range | 8..16 | 1..256 | How far from you particles appear, in blocks. |
| WorldParticles → [Simple] → Count | Integer | 256 | 32..1024 | Most particles at once. |
| WorldParticles → [Simple] → Size | Decimal | 1.0 | 0.1..10.0 | Particle size. |
| WorldParticles → [Simple] → Life | Integer Range | 20..30 | 1..512 | How long each particle stays. |
| WorldParticles → [Simple] → SpawnTime | Integer | 25 ms | 1..200 ms | Time between new particles. |
| WorldParticles → [Simple] → AnimCurve | Choice | QuadInOut | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How particles grow and shrink. |
| WorldParticles → [Simple] → CanBeCovered | Toggle | true | | Blocks can hide particles. Off shows them through walls. |
| WorldParticles → [Simple] → YMotion | Toggleable Group | Off | | Makes particles drift up or down. |
| WorldParticles → [Simple] → YMotion → Motion | Decimal | 2.0 | -10.0..10.0 | How far they drift. Negative goes down. |
| WorldParticles → [Simple] → YMotion → AnimBy | Choice | Progress | Progress, Age | What the drift follows. |
| WorldParticles → [Simple] → Particle | Choice | Spark | Orbiz, Star, Dollar, Crown, Heart, Lightning, Line, Point, Rhombus, Snowflake, Spark | Particle picture. |
| WorldParticles → [Simple] → Color → Color | Color | Light blue | | Particle color. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/customambience/ModuleCustomAmbience.kt)*
