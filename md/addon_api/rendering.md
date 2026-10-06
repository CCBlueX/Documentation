## Rendering

Modules draw in two events: `OverlayRenderEvent` for the screen, `WorldRenderEvent` for the world. [HUD components](/docs/add-on-api/developers/hud-components) use the same overlay drawing.

### On the screen

`OverlayRenderEvent` is raised while the HUD is drawn. `event.context` is Minecraft's `GuiGraphicsExtractor`, positions are in GUI-scaled pixels.

```kotlin
object ModuleCoordinates : ClientModule("Coordinates", ModuleCategories.RENDER) {

    private val color by color("Color", Color4b.WHITE)

    @Suppress("unused")
    private val overlayHandler = handler<OverlayRenderEvent> { event ->
        val text = Component.literal("%.1f %.1f %.1f".format(player.x, player.y, player.z))
        val font = FontManager.FONT_RENDERER
        val x = mc.window.guiScaledWidth / 2f
        val width = font.getStringWidth(text)

        event.context.drawQuad(x - width / 2 - 2, 2f, x + width / 2 + 2, 14f, Color4b(0, 0, 0, 120))
        font.draw(event.context, text, x, 4f, color, shadow = true, horizontalAnchor = HorizontalAnchor.CENTER)
    }

}
```

#### `drawQuad(x1, y1, x2, y2, fillColor, outlineColor)`
Draws a rectangle between two corners, an extension of `GuiGraphicsExtractor`. <br>

| Property     | Description                             | Required | Type       | Default       |
|--------------|-----------------------------------------|----------|------------|---------------|
| x1, y1       | One corner.                             | Yes      | `Float`    |               |
| x2, y2       | The opposite corner.                    | Yes      | `Float`    |               |
| fillColor    | Fill, `null` or transparent for none.   | No       | `Color4b?` | transparent   |
| outlineColor | Outline, `null` or transparent for none.| No       | `Color4b?` | transparent   |

<hr>

#### `FontManager.FONT_RENDERER.draw(context, text, x, y, color, shadow, scale, horizontalAnchor, verticalAnchor)`
Draws text with the client's font and returns the width drawn. <br>

| Property         | Description                                                            | Required | Type               | Default               |
|------------------|------------------------------------------------------------------------|----------|--------------------|-----------------------|
| context          | `event.context`.                                                       | Yes      | `GuiGraphicsExtractor` |                   |
| text             | Text, formatting codes and styles apply.                               | Yes      | `Component`        |                       |
| x, y             | Position.                                                              | Yes      | `Float`            |                       |
| color            | Color where the text sets none.                                        | No       | `Color4b`          | `Color4b.WHITE`       |
| shadow           | Draw a shadow.                                                         | No       | `Boolean`          | `false`               |
| scale            | 1 is the font's own size, the default matches Minecraft's font.        | No       | `Float`            | Minecraft's size      |
| horizontalAnchor | Which point of the text `x` refers to: `START`, `CENTER` or `END`.     | No       | `HorizontalAnchor?`| start                 |
| verticalAnchor   | Which point of the text `y` refers to: `TOP`, `MIDDLE` or `BOTTOM`.    | No       | `VerticalAnchor?`  | top                   |

`getStringWidth(text)` measures text at the same default scale.

Everything Minecraft's own `GuiGraphicsExtractor` offers can be used as well.

### In the world

`WorldRenderEvent` is raised while the world is drawn. `renderEnvironment` gives access to the drawing functions, `withPositionRelativeToCamera` moves the origin to a position in the world:

```kotlin
object ModuleWaypoint : ClientModule("Waypoint", ModuleCategories.RENDER) {

    private val position by vec3i("Position", Vec3i(0, 64, 0))
    private val color by color("Color", Color4b(255, 200, 0, 80))

    @Suppress("unused")
    private val renderHandler = handler<WorldRenderEvent> { event ->
        val pos = BlockPos(position.x, position.y, position.z)

        event.renderEnvironment {
            withPositionRelativeToCamera(pos) {
                drawBox(FULL_BOX, color, color.alpha(255))
            }

            withPositionRelativeToCamera {
                drawLine(player.getEyePosition(event.partialTicks), Vec3.atCenterOf(pos), color.alpha(255).argb)
            }
        }
    }

}
```

`withPositionRelativeToCamera` takes a `BlockPos`, a `Vec3` or `x, y, z`. Without a position, the origin is the world's, so world coordinates can be passed as they are. `event.partialTicks` interpolates positions between ticks.

#### `drawBox(box, faceColor, outlineColor)`
Draws an `AABB` relative to the current origin. `FULL_BOX` is one block, `BlockPos.outlineBox` the outline of the block at that position, both relative to the block's corner. <br>

| Property     | Description                                   | Required | Type       | Default     |
|--------------|-----------------------------------------------|----------|------------|-------------|
| box          | The box.                                      | Yes      | `AABB`     |             |
| faceColor    | Faces, `null` or transparent for none.        | No       | `Color4b?` | transparent |
| outlineColor | Edges, `null` or transparent for none.        | No       | `Color4b?` | transparent |
| noDepthTest  | Draw through blocks.                          | No       | `Boolean`  | `true`      |

<hr>

#### `drawLine(p1, p2, argb)`
Draws a line between two points relative to the current origin, through blocks. <br>

| Property | Description          | Required | Type   | Default |
|----------|----------------------|----------|--------|---------|
| p1, p2   | The end points.      | Yes      | `Vec3` |         |
| argb     | Color, `Color4b.argb`. | Yes    | `Int`  |         |

### Colors

`Color4b` is the client's color type, used by settings and every drawing function.

| Member                                   | Description                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| `Color4b(r, g, b, a)`                    | From channels 0 to 255, `a` defaults to 255.                         |
| `Color4b(argb)`                          | From a packed ARGB `Int`.                                            |
| `Color4b.fromHex("#RRGGBB")`             | From `#RRGGBB` or `#AARRGGBB`.                                       |
| `WHITE`, `BLACK`, `RED`, `LIQUID_BOUNCE`, ... | Constants, also `TRANSPARENT`.                                  |
| `r`, `g`, `b`, `a`, `argb`               | The channels and the packed value.                                   |
| `alpha(a)`                               | The same color with another alpha.                                   |
| `fade(f)`                                | The alpha multiplied by `f`.                                         |
| `darker()`                               | Each channel at 70 %.                                                |
| `interpolateTo(other, t)`                | Between this color (`t = 0`) and `other` (`t = 1`).                  |
| `Color4b.ofHSB(h, s, b)`                 | From hue, saturation and brightness.                                 |

### From Java

The drawing functions are Kotlin extension functions, which Java calls as static methods with the receiver first:

```java
RenderShortcutsKt.withPositionRelativeToCamera(event.getEnvironment(), found, env ->
    RenderShortcutsKt.drawBox(env, RenderShortcutsKt.FULL_BOX, new Color4b(255, 0, 0, 80), Color4b.RED));

Render2DKt.drawQuad(event.getContext(), 4f, 4f, 8f + width, 16f, new Color4b(0, 0, 0, 120));
FontManager.getFONT_RENDERER().draw(event.getContext(), text, 6f, 6f);
```
