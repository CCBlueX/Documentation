## CustomAmbience

CustomAmbience lets you take over how the world around you looks, regardless of the actual server-side weather, time of day, fog, lighting, or sky color. Want a permanent snowy night even on a sunny survival server, or a clear sky with no rain blocking your view? This module forces the client to render whatever ambience you choose, purely on your screen.

Everything here is visual and local to your client — it does not change the real game state, so other players still see the server's normal weather and time. You can mix and match: set a time and weather, then optionally fine-tune precipitation density, fog distances and color, the lightmap (overall scene tint), and the sky color. Leave any choice on `NoChange` to keep the server's real value for that aspect.

A common use is comfort and visibility: clearing fog, brightening or recoloring the lightmap, or locking a pleasant time of day. It pairs well with other render tweaks like [FullBright](/docs/modules/render/fullbright) and [AntiBlind](/docs/modules/render/antiblind).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Weather | Choice | Snowy | NoChange, Sunny, Rainy, Snowy, Thunder | Forces the displayed weather effect, or keeps the server's weather on NoChange. |
| Time | Choice | Night | NoChange, Dawn, Day, Noon, Dusk, Night, MidNight | Locks the visual time of day, or keeps the server's time on NoChange. |
| ModifyPrecipitation | Toggleable Group | On | — | Adjusts how rain and snow are rendered. |
| ModifyPrecipitation → Gradient | Decimal | 0.7 | 0.1..1.0 | Controls how dense and heavy the falling rain or snow appears. |
| Fog | Toggleable Group | On | — | Overrides the world's fog rendering. |
| Fog → DisableWorldFog | Toggle | false | — | Removes the world fog entirely for a clearer view. |
| Fog → BackgroundColor | Color | — | — | Sets the color the distant background and fog fade into. |
| Fog → Environmental | Decimal Range | 0.0..0.0 | -16.0..2048.0 | Sets the near and far distances over which environmental fog fades in. |
| Fog → RenderDistance | Decimal Range | 0.0..0.0 | 0.0..1024.0 | Sets the near and far distances over which render-distance fog fades in. |
| Fog → SkyEnd | Decimal | 0.0 | 0.0..1024.0 | Distance at which the sky fog ends. |
| Fog → CloudEnd | Decimal | 0.0 | 0.0..4096.0 | Distance at which the cloud fog ends. |
| CustomLightmap | Toggleable Group | Off | — | Overrides the scene's lighting with a custom tint. |
| CustomLightmap → Mode | Mode Selector | SingleColor | SingleColor | Selects how the lightmap is overridden. |
| CustomLightmap → Mode → [SingleColor] → Color | Color | — | — | The single color applied across the whole lightmap. |
| SkyColor | Toggleable Group | Off | — | Overrides the sky with a chosen color. |
| SkyColor → Color | Color | — | — | The color used to paint the sky. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleCustomAmbience.kt)*
