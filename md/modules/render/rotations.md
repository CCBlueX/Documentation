## Rotations

Rotations makes your client-side character model reflect the server-side rotations being sent by combat modules such as [KillAura](/docs/modules/combat/killaura), [Aimbot](/docs/modules/combat/aimbot), or [CrystalAura](/docs/modules/combat/crystalaura). Without this module, your character visually faces wherever you are looking — even though the server sees a different yaw and pitch. Enabling Rotations keeps what you see consistent with what the server registers, so you can tell at a glance where your character is actually aiming.

You can choose which body parts follow the server rotation (head, body, or both) and optionally add a small amount of visual smoothing so rapid rotation snapping appears less jarring on screen. Two optional overlays — a line and a dot — can be enabled by setting their alpha above zero, drawing a vector in the world that shows the exact direction of the current server-side rotation in real time.

This module is enabled by default because it is a purely visual aid with no gameplay downside; disabling it simply causes your character model to stop mirroring server rotations.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| BodyPart | Multi-Select | Head, Body | Head, Body | Which body parts visually follow the server-side rotation. Select Head, Body, or both. |
| Smooth | Decimal | 0.0 | 0.0–0.3 | Visually interpolates the model rotation toward the server rotation each tick. Higher values create a smoother but slightly delayed appearance. Set to 0.0 to disable smoothing. |
| VectorLine | Color | — | — | Color (including alpha) of the line drawn from your eye position toward the server-side aim direction. Set alpha to 0 to hide the line. |
| VectorDot | Color | — | — | Color (including alpha) of the dot drawn at the end of the server-side aim vector. Set alpha to 0 to hide the dot. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleRotations.kt)*
