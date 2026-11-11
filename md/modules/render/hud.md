## HUD

HUD shows the client's overlay on your screen, like the module list and other parts of the active theme. It is on by default. When you hide the normal game HUD (F1), the overlay hides too.

**Themes** holds the settings of your installed themes. **AdditionalComponents** has extra parts drawn by the client, like the minimap.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Blur | Toggleable Group | On | | Blurs the game behind overlay panels. |
| Blur → Sigma | Decimal | 5.0 | 1.0 to 15.0 | How strong the blur is. |
| Blur → AlphaBlendRange | Decimal Range | 0.0 to 0.75 | 0.0 to 1.0 | Where the blur blends from no blur to full blur. |
| SpaceSeperatedNames | Toggle | true | | Writes module names with spaces, like "Kill Aura" instead of "KillAura". |
| Themes | Setting Group | | | Settings of your installed themes. |
| AdditionalComponents | Setting Group | | | Extra overlay parts. |
| AdditionalComponents → Minimap | Toggleable Group | Off | | Shows a small map of the land and entities around you. |
| AdditionalComponents → Minimap → Alignment → Horizontal | Choice | Left | Left, Center, CenterTranslated, Right | Which side of the screen the map sticks to. |
| AdditionalComponents → Minimap → Alignment → HorizontalOffset | Integer | 7 | -1000 to 1000 | Moves the map left or right. |
| AdditionalComponents → Minimap → Alignment → Vertical | Choice | Top | Top, Center, CenterTranslated, Bottom | Whether the map sticks to the top or bottom. |
| AdditionalComponents → Minimap → Alignment → VerticalOffset | Integer | 180 | -1000 to 1000 | Moves the map up or down. |
| AdditionalComponents → Minimap → Size | Integer | 96 | 1 to 256 | Size of the map. |
| AdditionalComponents → Minimap → ViewDistance | Decimal | 3.0 | 1.0 to 8.0 | How far the map shows, in chunks. |
| AdditionalComponents → Minimap → FixedDirection | Toggle | false | | Keeps north up instead of turning the map with you. |
| AdditionalComponents → Minimap → Texture | Toggleable Group | On | | Draws the land on the map. |
| AdditionalComponents → Minimap → Texture → VertexColor | Color | White | | Tints the land. |
| AdditionalComponents → Minimap → Entity | Toggleable Group | On | | Shows entities on the map. |
| AdditionalComponents → Minimap → Entity → Scale | Decimal | 1.0 | 0.25 to 4.0 | Size of the entity markers. |
| AdditionalComponents → Minimap → Entity → OutOfBounds | Choice | None | None, All | With All, entities outside the map get a marker on its edge. |
| AdditionalComponents → Minimap → Compass | Toggleable Group | Off | | Shows a compass on the map. |
| AdditionalComponents → Minimap → Compass → Placement | Choice | TopLeft | TopLeft, TopRight, BottomLeft, BottomRight | Which corner the compass is in. |
| AdditionalComponents → Minimap → Clock | Toggleable Group | Off | | Shows a clock on the map. |
| AdditionalComponents → Minimap → Clock → Placement | Choice | TopLeft | TopLeft, TopRight, BottomLeft, BottomRight | Which corner the clock is in. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleHud.kt)*
