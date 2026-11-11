## RotationManager

When a module like [KillAura](/docs/modules/combat/killaura) turns your character toward a target, your camera stays where you are looking. The RotationManager global setting makes your character model in third person show the direction the module is actually aiming. It can also draw a line and a dot that point the same way.

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| BodyPart | Multi-Select | Head, Body | Head, Body | Which parts of your model turn to show the aim direction. |
| VectorLine | Color | White, alpha 0 | | Color of a line pointing where you aim. It is hidden while the alpha is 0, so raise the alpha to show it. |
| VectorDot | Color | Blue, alpha 0 | | Color of a dot where you aim. It is hidden while the alpha is 0. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/aiming/RotationManager.kt)*
