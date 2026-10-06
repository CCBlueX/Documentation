## NoFOV

NoFOV keeps your field of view from changing due to in-game events. In vanilla Minecraft, sprinting, drawing a bow, being affected by speed or slowness potions, and riding a mount all dynamically shift your FOV. With this module enabled, those shifts are suppressed or replaced, giving you a consistent view at all times.

**Constant** mode is the simplest option: it replaces whatever FOV Minecraft would display with a single fixed degree value. If you just want a steady, unchanging field of view, this is the mode to use. **Custom** mode instead intercepts the internal FOV multiplier Minecraft calculates and remaps it — you can set a base offset, scale how strongly dynamic changes carry through, and clamp the result to a specific range. This is useful if you want to preserve a small amount of FOV feedback while still preventing extreme swings.

NoFOV pairs naturally with [Zoom](/docs/modules/render/zoom) if you frequently switch between a wide field of view and a zoomed-in perspective, since both modules work on how the camera FOV is presented to you.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Constant | — | Selects how the FOV override is applied: a fixed degree value or a custom multiplier remap. |
| Mode → [Constant] → FOV | Integer | 115 | 1–179 | The fixed FOV in degrees used at all times when Constant mode is active. |
| Mode → [Custom] → BaseFOV | Decimal | 1.0 | 0.0–1.5 | Base FOV multiplier added as an offset after the dynamic component is scaled. |
| Mode → [Custom] → Limit | Decimal Range | 0.0–1.5 | 0.0–1.5 | Clamps the final FOV multiplier to this range, preventing it from going below or above the set bounds. |
| Mode → [Custom] → Multiplier | Decimal | 1.0 | 0.1–1.5 | Scales how strongly the dynamic (movement/effect-driven) FOV component carries through. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleNoFov.kt)*
