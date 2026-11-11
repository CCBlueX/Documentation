## ScrollAdjust

ScrollAdjust lets you change a value by scrolling the mouse wheel while you play. Hold the Modifier key and scroll. In [CameraClip](/docs/modules/render/cameraclip) this changes how far away the third person camera is. In [AirPlace](/docs/modules/world/airplace) it changes how far away you place blocks.

Used by: [AirPlace](/docs/modules/world/airplace), [CameraClip](/docs/modules/render/cameraclip).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ScrollAdjust | Toggleable Group | On | | Turns scroll changing on or off. |
| Modifier | Key | Left Alt (CameraClip: Left Control) | | The key you hold while scrolling. With no key set, every scroll changes the value. |
| Sensitivity | Decimal | 0.5 (CameraClip: 0.3) | 0.1..1.0 (CameraClip: 0.1..2.0) | How much each scroll step changes the value. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/cameraclip/ScrollAdjustValueGroup.kt)*
