## CameraClip

CameraClip lets your third-person camera go through walls. Normally the camera moves close to you when a block is behind you. With this on, it stays at the distance you set, and you can push it much farther back.

With ScrollAdjust on, hold Left Control and scroll to move the camera closer or farther.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| CameraDistance | Decimal | 4.0 | 1.0..48.0 | How far behind you the camera is. |
| Animation | Toggleable Group | On | | Moves the camera smoothly when its distance changes. |
| Animation → Speed | Decimal | 0.6 | 0.1..1.0 | How fast the camera moves. |
| Animation → Easing | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the movement speeds up and slows down. |
| ScrollAdjust | Toggleable Group | On | | Change the distance with the mouse wheel. See [Shared: ScrollAdjust](/docs/modules/shared-settings/scrolladjust). |
| ScrollAdjust → Modifier | Key | Left Control | | Key you hold while scrolling. With no key set, scrolling always works. |
| ScrollAdjust → Sensitivity | Decimal | 0.3 | 0.1..2.0 | How much one scroll step changes the distance. |
| ScrollAdjust → RememberScrolled | Toggle | false | | Keeps the distance you scrolled to as your new CameraDistance. |
| ScrollAdjust → RequireFreeLook | Toggle | false | | Scrolling only works while [FreeLook](/docs/modules/render/freelook) is on. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/cameraclip/ModuleCameraClip.kt)*
