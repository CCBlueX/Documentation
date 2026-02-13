## TargetRendering

A visual indicator rendered on or near the currently targeted entity. Used across several combat modules to give visual feedback about which entity is being targeted.

This is a toggleable group (can be enabled/disabled).

### Modes

**Legacy** - Renders a flat 3D box above the target entity's head. The box is centered horizontally on the entity and positioned at the top of the entity's bounding box plus an extra Y offset.

Sub-settings:

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Size | Float | 0.5 | 0.1–2.0 | Half-width of the box on the X and Z axes. |
| Height | Float | 0.1 | 0.02–2.0 | Vertical thickness of the box. |
| Color | Color | LiquidBounce theme (alpha 100) | — | Color of the box. |
| ExtraYOffset | Float | 0.1 | 0.0–1.0 | Additional vertical offset above the entity's bounding box top. |

**Circle** - Renders a flat gradient-filled circle in the world at the target's position. The circle is drawn as a gradient from `OuterColor` at the rim to `InnerColor` at the center, with an optional outline ring on top. The outline is hidden when its color is fully transparent.

Sub-settings:

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Radius | Float | 0.85 | 0.1–2.0 | Outer radius of the circle. |
| InnerRadius | Float | 0.0 | 0.0–2.0 | Radius of the inner gradient endpoint. Clamped to not exceed Radius. |
| HeightMode | Mode | — | — | Determines the vertical position of the circle. See [HeightMode](#heightmode-shared-sub-mode). |
| OuterColor | Color | LiquidBounce theme (alpha 100) | — | Color at the outer edge of the gradient. |
| InnerColor | Color | LiquidBounce theme (alpha 100) | — | Color at the inner center of the gradient. |
| Color | Color | #007CFF (full alpha) | — | Outline color drawn around the outer edge. Set to transparent to hide the outline. |

**Image** - Renders a textured quad in the world at the target's position, always facing the camera (billboard). Supports both a custom user-provided image and built-in preset textures (Marker1, Marker2). The quad can be rotated over time using an animation curve.

Sub-settings:

| Setting | Type | Default | Description |
|---|---|---|---|
| Source | Mode | Custom | Image source. Choose between **Custom** (user-provided texture) and **Builtin** (preset textures: Marker1, Marker2). |
| Scale | Vec2f | (1.0, 1.0) | X and Y scale of the rendered quad. |
| ColorModulator | Color | White | Tint color multiplied onto the texture. |
| Rotate | AnimatedValueGroup | — | Animation curve controlling rotation over time. The curve maps a progress value (0–1) to degrees (-180–180). |
| HeightMode | Mode | — | Determines the vertical position of the image. See [HeightMode](#heightmode-shared-sub-mode). |

**GlowingCircle** - Renders a solid filled circle with a vertical glow effect extending upward or downward from the circle plane. The glow is drawn as a gradient cone from `OuterColor` at the base to `GlowColor` at the glow tip. An optional outline is drawn around the base circle. When using the Animated or Health height modes, the glow height is calculated automatically; otherwise the `GlowHeight` setting controls it.

Sub-settings:

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Radius | Float | 0.85 | 0.1–2.0 | Radius of the circle. |
| HeightMode | Mode | — | — | Determines the vertical position of the circle. See [HeightMode](#heightmode-shared-sub-mode). |
| OuterColor | Color | LiquidBounce theme (alpha 100) | — | Color of the solid circle fill and base of the glow gradient. |
| GlowColor | Color | LiquidBounce theme (alpha 0) | — | Color at the tip of the glow gradient. |
| GlowHeight | Float | 0.3 | -1.0–1.0 | Vertical offset of the glow tip relative to the circle. Ignored when the active HeightMode provides its own glow height (Animated). |
| Color | Color | #007CFF (full alpha) | — | Outline color drawn around the circle. Set to transparent to hide the outline. |

**Ghost** - Renders three spiraling particle trails around the target entity using a glow texture. Each trail follows a different 3D path computed from sine and cosine functions. The particles are billboarded (always face the camera) and fade out progressively along the trail. The trail orbits continuously based on the client uptime.

Sub-settings:

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Color | Color | Blue | — | Base color of the particles. Alpha fades along the trail. |
| Size | Float | 0.5 | 0.4–0.7 | Size of each individual particle quad. |
| Length | Int | 25 | 15–40 | Number of particles per trail. Longer values produce a longer spiral with more fade. Also affects the orbit radius slightly. |

**Text2D** - Projects text onto the screen at the target's world position using screen-space rendering. The text is drawn using the client's font renderer, centered horizontally and vertically on the projected point. Supports multiple lines of text and optional text shadow.

Sub-settings:

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Scale | Float | 1.0 | 0.01–10.0 | Scale factor for the rendered text. |
| Shadow | Boolean | true | — | Whether to draw a shadow behind the text. |
| Color | Color | Red | — | Color applied to the text via the text style. |
| Text | Text List | ["TARGET"] | — | List of text lines to display. Each line is rendered below the previous one. |
| HeightMode | Mode | — | — | Determines the vertical world position before screen projection. See [HeightMode](#heightmode-shared-sub-mode). |

**Arrow** - Projects a downward-pointing triangle onto the screen above the target entity's head. The triangle tip points at the top of the entity's bounding box. The triangle width is `10 × Size` and its height is `10 × Size`.

Sub-settings:

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Color | Color | Red | — | Fill color of the triangle. |
| OutlineColor | Color | Transparent | — | Outline color of the triangle. Hidden when transparent. |
| Size | Float | 1.5 | 0.5–20.0 | Scale factor for the triangle dimensions. |

### HeightMode (shared sub-mode)

Used by Circle, Image, GlowingCircle, and Text2D to determine the vertical world position at which the indicator is rendered relative to the target entity.

**Feet** - Positions the indicator at the entity's foot level (Y = 0 relative to entity position).

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Offset | Float | 0.0 | -1.0–1.0 | Additional vertical offset from the feet position. |

**Top** - Positions the indicator at the top of the entity's bounding box.

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Offset | Float | 0.0 | -1.0–1.0 | Additional vertical offset from the top of the bounding box. |

**Relative** - Positions the indicator at a fraction of the entity's total height. A value of 0 corresponds to the feet, 1 corresponds to the top of the bounding box.

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Height | Float | 0.5 | -0.5–1.5 | Fraction of entity height at which to place the indicator. |

**Health** - Positions the indicator based on the entity's current health percentage. The height is calculated as `(currentHealth / maxHealth) × entityHeight`. Falls back to 0 for non-living entities.

No additional settings.

**Animated** - Moves the indicator up and down over time using a sine wave. The position follows the formula `sin(tickCount × Speed) × HeightMultiplier + HeightOffset`. Also provides an automatic glow height offset for GlowingCircle.

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Speed | Float | 0.18 | 0.01–1.0 | Speed multiplier for the sine wave oscillation. |
| HeightMultiplier | Float | 0.4 | 0.1–1.0 | Amplitude of the vertical oscillation. |
| HeightOffset | Float | 1.3 | 0.0–2.0 | Baseline vertical offset around which the sine wave oscillates. |
| GlowOffset | Float | -1.0 | -3.1–3.1 | Phase offset applied to the sine wave when calculating the glow height for GlowingCircle. |

---
*Last updated: 2026-02-13*
