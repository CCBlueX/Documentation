## Placement Rendering

Placement Rendering controls the animated boxes that modules draw onto blocks in the world — for example, the boxes [CrystalAura](/docs/modules/combat/crystalaura) shows on placement spots, the blocks [Scaffold](/docs/modules/world/scaffold) lays down, or the blocks [Nuker](/docs/modules/world/nuker) and [PacketMine](/docs/modules/world/packetmine) are breaking. Whenever one of these modules marks a block, this group decides how that box looks and how it animates in and out.

You can tune the look in two ways: the **appearance** (the fill color, the outline color, and whether neighbouring boxes are merged into one clean shape) and the **animation** (how the box grows in when it appears, shrinks away when it's removed, and how quickly it fades). Longer times and softer curves give smooth, subtle visuals, while short times make boxes snap in and out instantly.

Turning on **Clump** is handy when a module marks many blocks at once: instead of a grid of separate cubes, touching blocks are drawn as a single connected outline, which looks cleaner and is easier to read at a glance.

This setting group is used by the following modules:

- [CrystalAura](/docs/modules/combat/crystalaura)
- [Fucker](/docs/modules/world/fucker)
- [Notebot](/docs/modules/fun/notebot)
- [Nuker](/docs/modules/world/nuker)
- [PacketMine](/docs/modules/world/packetmine)
- [ProphuntESP](/docs/modules/render/prophuntesp)
- [Scaffold](/docs/modules/world/scaffold)
- [VoidESP](/docs/modules/render/voidesp)

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Clump | Toggle | false | — | Merges touching boxes into one continuous shape, hiding the inner faces and edges between neighbouring blocks so a cluster looks like a single solid outline instead of separate cubes. |
| StartSize | Decimal | 1.0 | 0.0..2.0 | The size a box starts at when it first appears, as a multiplier of the block's normal size. `1.0` starts at full size; lower values make the box grow into place, higher values make it shrink into place. |
| StartCurve | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | The easing curve used for the grow-in (appear) animation, controlling how the box eases toward its full size. |
| EndSize | Decimal | 0.8 | 0.0..2.0 | The size a box shrinks (or grows) to as it fades out and disappears, as a multiplier of the block's normal size. |
| EndCurve | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | The easing curve used for the shrink-out (disappear) animation. |
| FadeInCurve | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | The easing curve for how a box's color and opacity fade in as it appears. |
| FadeOutCurve | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | The easing curve for how a box's color and opacity fade out as it disappears. |
| InTime | Integer | 500 | 0..5000 (ms) | How long the appear animation (grow-in and fade-in) takes, in milliseconds. `0` makes boxes pop in instantly. |
| OutTime | Integer | 500 | 0..5000 (ms) | How long the disappear animation (shrink-out and fade-out) takes, in milliseconds. `0` makes boxes vanish instantly. |
| Color | Color | — | — | The fill color and transparency of the box. |
| OutlineColor | Color | — | — | The color of the box's outline edges. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/utils/render/placement/PlacementRenderer.kt)*
