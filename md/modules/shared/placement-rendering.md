## Placement Rendering

Placement Rendering draws boxes on blocks a module is working on, for example where [CrystalAura](/docs/modules/combat/crystalaura) places crystals or which blocks [Nuker](/docs/modules/world/nuker) breaks. The boxes grow in when they show up and fade away when they are done. Here you pick their colors and how they move.

Used by: [CrystalAura](/docs/modules/combat/crystalaura), [Fucker](/docs/modules/world/fucker), [Notebot](/docs/modules/fun/notebot), [Nuker](/docs/modules/world/nuker), [PacketMine](/docs/modules/world/packetmine), [ProphuntESP](/docs/modules/render/prophuntesp), [Scaffold](/docs/modules/world/scaffold), [VoidESP](/docs/modules/render/voidesp), [Block Placer](/docs/modules/shared-settings/block-placer).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Clump | Toggle | depends on the module | | Joins boxes that touch into one big shape. On in most modules, off in CrystalAura. |
| StartSize | Decimal | 1.0 | 0.0..2.0 | How big a box is when it shows up. 1.0 is the size of a block. |
| StartCurve | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the box grows or shrinks when it shows up. None jumps straight to the end. |
| EndSize | Decimal | 0.8 | 0.0..2.0 | How big a box gets while it goes away. |
| EndCurve | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the box grows or shrinks while it goes away. |
| FadeInCurve | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the box fades in. |
| FadeOutCurve | Choice | Linear | Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None | How the box fades out. |
| InTime | Integer | 500 | 0..5000 ms | How long showing up takes. 0 shows it right away. |
| OutTime | Integer | 500 | 0..5000 ms | How long going away takes. 0 removes it right away. |
| Color | Color | | | Color inside the box. |
| OutlineColor | Color | | | Color of the box's edges. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/render/placement/PlacementRenderer.kt)*
