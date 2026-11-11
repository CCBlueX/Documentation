## TargetRendering

TargetRendering draws a mark on the player or mob a module is targeting, so you can see who it is going after. You can pick from several looks, like a glowing circle, a picture or floating hearts.

Used by: [KillAura](/docs/modules/combat/killaura), [Aimbot](/docs/modules/combat/aimbot), [AutoBow](/docs/modules/combat/autobow), [AutoRod](/docs/modules/combat/autorod), [AutoShoot](/docs/modules/combat/autoshoot), [CrystalAura](/docs/modules/combat/crystalaura), [ElytraTarget](/docs/modules/combat/elytratarget), [BlockTrap](/docs/modules/world/blocktrap).

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| TargetRendering | Toggleable Group | On | | Turns the mark on or off. |
| Mode | Choice | GlowingCircle | Legacy, Circle, Image, GlowingCircle, Ghost, Hearts, Text2D, Arrow | What the mark looks like. |
| Mode → [Legacy] → Size | Decimal | 0.5 | 0.1..2.0 | How wide the flat box above the target's head is. |
| Mode → [Legacy] → Height | Decimal | 0.1 | 0.02..2.0 | How thick the box is. |
| Mode → [Legacy] → Color | Color | | | Color of the box. |
| Mode → [Legacy] → ExtraYOffset | Decimal | 0.1 | 0.0..1.0 | How far above the head the box floats. |
| Mode → [Circle] → Radius | Decimal | 0.85 | 0.1..2.0 | How big the circle is. |
| Mode → [Circle] → InnerRadius | Decimal | 0.0 | 0.0..2.0 | Size of the middle part where the color changes to InnerColor. |
| Mode → [Circle] → HeightMode | Choice | Feet | Feet, Top, Relative, Health, Animated | How high on the target it is drawn. See [HeightMode](#heightmode) below. |
| Mode → [Circle] → OuterColor | Color | | | Color at the edge. |
| Mode → [Circle] → InnerColor | Color | | | Color in the middle. |
| Mode → [Circle] → Color | Color | Blue | | Color of the line around the edge. Make it see-through to hide it. |
| Mode → [Image] → Source | Choice | Custom | Custom, Builtin | Where the picture comes from. Custom uses a PNG or JPG file you pick. Builtin uses one that comes with the client. |
| Mode → [Image] → Source → [Custom] → File | File | | | Your picture file. |
| Mode → [Image] → Source → [Builtin] → Preset | Choice | Marker1 | Marker1, Marker2 | Which built-in picture to use. |
| Mode → [Image] → Scale | Vector | 1.0, 1.0 | | How wide and how tall the picture is. |
| Mode → [Image] → ColorModulator | Color | White | | Tints the picture with this color. |
| Mode → [Image] → Rotate → Period | Integer | 1000 | 10..20000 ms | How long one turn of the animation takes. |
| Mode → [Image] → Rotate → Symmetric | Toggle | true | | Plays the animation forward and then backward. |
| Mode → [Image] → Rotate → Curve | Curve | | | How far the picture is turned over time, in degrees. |
| Mode → [Image] → HeightMode | Choice | Feet | Feet, Top, Relative, Health, Animated | How high on the target it is drawn. See [HeightMode](#heightmode) below. |
| Mode → [GlowingCircle] → Radius | Decimal | 0.85 | 0.1..2.0 | How big the circle is. |
| Mode → [GlowingCircle] → HeightMode | Choice | Feet | Feet, Top, Relative, Health, Animated | How high on the target it is drawn. See [HeightMode](#heightmode) below. |
| Mode → [GlowingCircle] → OuterColor | Color | | | Color of the circle and the bottom of the glow. |
| Mode → [GlowingCircle] → GlowColor | Color | | | Color at the top of the glow. |
| Mode → [GlowingCircle] → GlowHeight | Decimal | 0.3 | -1.0..1.0 | How tall the glow is. Below 0 it glows downward. Not used with the Animated height mode. |
| Mode → [GlowingCircle] → Color | Color | Blue | | Color of the line around the edge. Make it see-through to hide it. |
| Mode → [Ghost] → Color | Color | Blue | | Color of the glowing trails that spin around the target. |
| Mode → [Ghost] → Size | Decimal | 0.5 | 0.4..0.7 | How big each glowing dot is. |
| Mode → [Ghost] → Length | Integer | 25 | 15..40 | How long the trails are. |
| Mode → [Hearts] → Color | Color | White | | Color of the health hearts. Extra (golden) hearts are always gold. |
| Mode → [Hearts] → DynamicCount | Toggle | true | | Shows as many hearts as the target has health. |
| Mode → [Hearts] → HeartCount | Integer | 10 | 1..32 | How many hearts to show when DynamicCount is off. |
| Mode → [Hearts] → YOffset | Decimal | 0.1 | -1.0..3.0 | How high the ring of hearts is. |
| Mode → [Hearts] → Size | Decimal | 0.15 | 0.05..1.0 | How big each heart is. |
| Mode → [Hearts] → Orbit → Radius | Decimal | 0.5 | 0.1..1.0 | How wide the ring of hearts is. |
| Mode → [Hearts] → Orbit → Speed | Decimal | 35.0 | -360.0..360.0 deg/s | How fast the hearts spin. Below 0 they spin the other way. |
| Mode → [Hearts] → Orbit → SqueezeStrength | Decimal | 0.25 | 0.0..1.0 | How much the ring gets squeezed flat while it spins. |
| Mode → [Hearts] → Orbit → SqueezeSpeed | Integer | 2 | 1..4 | How fast the squeezing goes. |
| Mode → [Hearts] → CanBeCovered | Toggle | false | | Lets blocks hide the hearts. |
| Mode → [Text2D] → Scale | Decimal | 1.0 | 0.01..10.0 | How big the text is. |
| Mode → [Text2D] → Shadow | Toggle | true | | Draws a shadow behind the text. |
| Mode → [Text2D] → Color | Color | Red | | Color of the text. |
| Mode → [Text2D] → Text | Text List | TARGET | | The text to show. Each entry is its own line. |
| Mode → [Text2D] → HeightMode | Choice | Feet | Feet, Top, Relative, Health, Animated | How high on the target it is drawn. See [HeightMode](#heightmode) below. |
| Mode → [Arrow] → Color | Color | Red | | Color of the arrow above the target's head. |
| Mode → [Arrow] → OutlineColor | Color | See-through | | Color of the arrow's edge. |
| Mode → [Arrow] → Size | Decimal | 1.5 | 0.5..20.0 | How big the arrow is. |

### HeightMode

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| [Feet] → Offset | Decimal | 0.0 | -1.0..1.0 | Draws it at the target's feet, moved up or down by this much. |
| [Top] → Offset | Decimal | 0.0 | -1.0..1.0 | Draws it at the top of the target's head, moved up or down by this much. |
| [Relative] → Height | Decimal | 0.5 | -0.5..1.5 | Draws it at this part of the target's height. 0 is the feet, 1 is the top. |
| [Health] | | | | Draws it higher the more health the target has. |
| [Animated] → Speed | Decimal | 0.18 | 0.01..1.0 | Moves it up and down. This is how fast. |
| [Animated] → HeightMultiplier | Decimal | 0.4 | 0.1..1.0 | How far it moves up and down. |
| [Animated] → HeightOffset | Decimal | 1.3 | 0.0..2.0 | The middle height it moves around. |
| [Animated] → GlowOffset | Decimal | -1.0 | -3.1..3.1 | For GlowingCircle: shifts the glow's movement against the circle's. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/utils/render/TargetRenderer.kt)*
