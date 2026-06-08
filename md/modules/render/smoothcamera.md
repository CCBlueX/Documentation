## SmoothCamera

SmoothCamera makes your camera position glide smoothly rather than snapping instantly to your player's movement. Instead of the camera jumping frame-to-frame, it interpolates toward the true position each tick, giving your gameplay a cinematic, fluid look — especially noticeable in third-person view while moving, bridging, or taking knockback.

By default the effect only applies in third-person perspectives, since first-person smoothing can feel disorienting during normal play. If you want the effect in first-person as well, enable **EnableFirstPOV**. The **HorizontalFactor** and **VerticalFactor** controls let you dial in exactly how "laggy" the camera feels: values closer to `1.0` make the camera trail further behind (more smoothing), while values closer to `0.0` make it snap almost instantly to your position (less smoothing). This module pairs well with [FreeCam](/docs/modules/render/freecam) or [AutoF5](/docs/modules/render/autof5) for screen-capture and recording setups where visual polish matters.

When you switch perspectives (e.g. first-person ↔ third-person), **ResetOnPerspectiveChange** snaps the camera immediately to your real position to avoid a jarring slide across the screen. Disable it only if you want a smooth transition between perspectives.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| EnableFirstPOV | Toggle | false | — | When enabled, the smoothing effect is also applied in first-person perspective. Disabled by default because it can feel unnatural during normal gameplay. |
| ResetOnPerspectiveChange | Toggle | true | — | Instantly snaps the camera to your real position whenever you switch perspectives, preventing a disorienting slide. |
| HorizontalFactor | Decimal | 0.9 | 0.0 – 1.0 | Controls how much horizontal smoothing is applied. Higher values make the camera trail further behind on the X/Z axes; lower values reduce the lag. |
| VerticalFactor | Decimal | 0.93 | 0.0 – 1.0 | Controls how much vertical smoothing is applied. Higher values make the camera trail further behind on the Y axis; lower values reduce the lag. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleSmoothCamera.kt)*
