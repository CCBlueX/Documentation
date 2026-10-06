## CameraClip

CameraClip lets the third-person camera pass through walls, floors, and other blocks instead of being pushed in close to your character whenever something is behind you. Normally Minecraft pulls the camera forward when it would clip into geometry; with this module the camera ignores those collisions, so you keep a clean, unobstructed view even when standing against a wall or in a tight space. It works by forcing the camera into "no-clip" mode during the [perspective handler](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/cameraclip/ModuleCameraClip.kt#L58-L61).

Use it whenever you want a stable third-person view — for recording, getting a wider field of awareness, or simply avoiding the jarring zoom that happens near surfaces. The base distance the camera sits at is set by **CameraDistance**, which can be pushed much farther out than vanilla allows.

Two optional groups refine the feel. **Animation** smoothly interpolates the camera between distances using an easing curve instead of snapping, via [a lerp on the current distance](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/cameraclip/ModuleCameraClip.kt#L67-L75). **ScrollAdjust** lets you change the camera distance on the fly with the mouse wheel (optionally while holding a modifier key), and can either snap back when you stop or remember your last distance — see the [scroll handling](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/cameraclip/ScrollAdjustValueGroup.kt#L53-L68).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| CameraDistance | Decimal | 4.0 | 1.0..48.0 | How far behind your character the third-person camera sits. Higher values pull the view back for a wider shot. |
| Animation | Toggleable Group | on | — | Smoothly interpolates the camera between distances instead of snapping when the distance or perspective changes. |
| Animation → Speed | Decimal | 0.6 | 0.1..1.0 | How quickly the camera catches up to the target distance each interpolation step. Higher is faster. |
| Animation → Easing | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | The easing curve applied to the animation, shaping how the camera accelerates and decelerates. |
| ScrollAdjust | Toggleable Group | on | — | Lets you change the camera distance live with the mouse wheel. Scrolling is clamped to the CameraDistance range and consumes the scroll so it won't switch hotbar slots. |
| ScrollAdjust → Modifier | Key | — | — | Optional key that must be held for scroll adjustment to apply (defaults to Left Control). If unbound, scrolling always adjusts. |
| ScrollAdjust → Sensitivity | Decimal | 0.3 | 0.1..2.0 | How much each scroll notch changes the camera distance. |
| ScrollAdjust → RememberScrolled | Toggle | false | — | When enabled, your scrolled distance is saved back into CameraDistance on reset instead of being discarded. |
| ScrollAdjust → RequireFreeLook | Toggle | false | — | When enabled, scroll adjustment only works while the FreeLook module is active. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/cameraclip/ModuleCameraClip.kt)*
