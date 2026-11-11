## FreeLook

FreeLook lets you turn the camera around your player while you keep walking and looking the same way. It only works while you hold its key. Let go and the camera goes back to normal.

Use it to see who is chasing you or to look around in a fight without turning your aim. Your player stays under your control, unlike with [FreeCam](/docs/modules/render/freecam).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Perspective | Choice | Back | Front, Back | Whether the camera looks at you from behind or from the front. |
| SenseBoost | Decimal | 1.0 | 0.1 to 2.0 | How fast the camera turns when you move the mouse. |
| NoPitchLimit | Toggle | true | | Lets the camera turn past straight up and straight down. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleFreeLook.kt)*
