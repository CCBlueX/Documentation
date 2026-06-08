## NoInterpolation

Minecraft smooths out entity movement between server updates using a process called interpolation — instead of entities snapping instantly to their new positions, the client gradually steps them there over several ticks. While this looks natural under normal conditions, it means what you see on screen can lag slightly behind where an entity actually is according to the server.

NoInterpolation reduces the number of interpolation steps the client uses, making entity position updates appear more immediate and snappy. This can be useful in combat situations where you want a more accurate, real-time picture of where other players or mobs are located, rather than a smoothed approximation.

Keep in mind this is a purely visual change — it does not affect server-side positions or hit registration. The higher the **ReduceBy** value, the more aggressively interpolation is cut down, with the maximum value of 3 effectively eliminating the smoothing steps entirely.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ReduceBy | Integer | 3 | 1–3 | How many interpolation steps to remove from entity movement updates. Higher values make position changes appear more immediate. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleNoInterpolation.kt)*
