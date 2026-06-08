## HUD

Shows an in-game overlay with various useful tools.

**Category:** Render  
**Enabled by default:** Yes

### Settings

Nested settings are shown with their group path, e.g. `Group → Setting`.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Blur | Toggleable Group | on | — |  |
| Blur → AlphaBlendRange | Decimal Range | 0.0..0.75 | 0.0..1.0 |  |
| SpaceSeperatedNames | Toggle | true | — |  |
| Themes | Setting Group | — | — |  |
| AdditionalComponents | Setting Group | — | — |  |
| AdditionalComponents → Minimap | Toggleable Group | off | — |  |
| AdditionalComponents → Minimap → Alignment | Setting Group | — | — |  |
| AdditionalComponents → Minimap → Alignment → Horizontal | Choice | Left | Left, Center, CenterTranslated, Right |  |
| AdditionalComponents → Minimap → Alignment → HorizontalOffset | Integer | 7 | -1000..1000 |  |
| AdditionalComponents → Minimap → Alignment → Vertical | Choice | Top | Top, Center, CenterTranslated, Bottom |  |
| AdditionalComponents → Minimap → Alignment → VerticalOffset | Integer | 180 | -1000..1000 |  |
| AdditionalComponents → Minimap → Size | Integer | 96 | 1..256 |  |
| AdditionalComponents → Minimap → ViewDistance | Decimal | 3.0 | 1.0..8.0 |  |
| AdditionalComponents → Minimap → FixedDirection | Toggle | false | — |  |
| AdditionalComponents → Minimap → Texture | Toggleable Group | on | — |  |
| AdditionalComponents → Minimap → Texture → VertexColor | Color | — | — |  |
| AdditionalComponents → Minimap → Entity | Toggleable Group | on | — |  |
| AdditionalComponents → Minimap → Entity → Scale | Decimal | 1.0 | 0.25..4.0 |  |
| AdditionalComponents → Minimap → Entity → OutOfBounds | Choice | None | None, All | Draws markers at the minimap edge for entities outside its view. `All` marks every tracked entity. |
| AdditionalComponents → Minimap → Compass | Toggleable Group | off | — |  |
| AdditionalComponents → Minimap → Compass → Placement | Choice | TopLeft | TopLeft, TopRight, BottomLeft, BottomRight |  |
| AdditionalComponents → Minimap → Clock | Toggleable Group | off | — |  |
| AdditionalComponents → Minimap → Clock → Placement | Choice | TopLeft | TopLeft, TopRight, BottomLeft, BottomRight |  |

### Screenshots

*Screenshots for HUD will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleHud.kt)*
