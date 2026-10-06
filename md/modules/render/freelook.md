## FreeLook

FreeLook lets you swing the camera around your character without changing the direction you're actually facing or moving. While the key is held, your view detaches from your aim — so you can glance behind you, check your flanks, or watch your surroundings while your player keeps walking and looking straight ahead. It's bound to a hold action, meaning the free camera is active only as long as you press the key, snapping back to normal the moment you release it.

This is handy for keeping an eye on chasers, lining up a third-person shot of yourself, or staying aware in PvP without committing your aim to a new direction. Unlike [FreeCam](/docs/modules/render/freecam), your body stays put and under your control — only the camera angle is freed.

Use **Perspective** to choose whether the detached camera sits behind or in front of you, **SenseBoost** to fine-tune how fast the camera turns relative to your normal mouse sensitivity, and **NoPitchLimit** to let the view roll past the usual straight-up/straight-down limits.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Perspective | Choice | Back | Front, Back | Whether the free camera looks from behind your character (Back) or faces it from the front (Front). |
| SenseBoost | Decimal | 1.0 | 0.1..2.0 | Multiplier for how quickly the camera turns as you move the mouse; lower for finer control, higher for faster sweeps. |
| NoPitchLimit | Toggle | true | — | When on, lets the camera tilt freely beyond the normal up/down limits instead of stopping at straight up or straight down. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleFreeLook.kt)*
