## SmoothCamera

SmoothCamera makes the camera glide after your player instead of moving with it right away. It looks smoother when you move, jump or take knockback, which is nice for recording. By default it only works in third person.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| EnableFirstPOV | Toggle | false | | Also smooths the camera in first person. |
| ResetOnPerspectiveChange | Toggle | true | | Moves the camera straight to your player when you switch views, so it does not slide across the screen. |
| HorizontalFactor | Decimal | 0.9 | 0.0 to 1.0 | How much the camera trails behind when you move sideways. Higher values trail more. |
| VerticalFactor | Decimal | 0.93 | 0.0 to 1.0 | How much the camera trails behind when you move up or down. Higher values trail more. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleSmoothCamera.kt)*
