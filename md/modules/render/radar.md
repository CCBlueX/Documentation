## Radar

Radar puts a small arrow on every entity around you, with its name next to it (and the head for players). When an entity is off screen or behind you, its arrow sticks to the edge of your screen and points toward it, so you always know which way to turn.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| OnlyPlayers | Toggle | false | | Only shows players and ignores mobs and other entities. |
| HideTeammates | Toggle | false | | Hides players on your team. See [Teams](/docs/modules/misc/teams). |
| Show | Multi-Select | InView, Offscreen | InView, Offscreen | **InView** shows arrows on entities you can see on screen. **Offscreen** shows arrows at the screen edge for entities you can't see. At least one must stay on. |
| EdgeInset | Decimal | 0.0 | 0.0 to 0.9 | Moves the edge arrows inward from the screen border. 0.1 keeps them 10% away from each edge. |
| PointerMode | Mode Selector | Triangle | Triangle, Image1, Image2 | Shape of the arrows. |
| PointerMode → Triangle → Width | Decimal | 8.0 | 1.0 to 100.0 | Width of the triangle. |
| PointerMode → Triangle → Height | Decimal | 10.0 | 1.0 to 100.0 | Height of the triangle. |
| PointerMode → Triangle → TailConcaveSize | Decimal | 2.0 | 0.0 to 50.0 | How deep the notch in the back of the triangle is. 0 gives a plain triangle. |
| PointerMode → Image1 → Size | Decimal | 10.0 | 1.0 to 100.0 | Size of the first arrow image. |
| PointerMode → Image2 → Size | Decimal | 10.0 | 1.0 to 100.0 | Size of the second arrow image. |
| ColorMode | Mode Selector | Distance | Distance, Health, Static, Rainbow | How arrows and names are colored. |
| ColorMode → Distance → Saturation | Decimal | 1.0 | 0.0 to 1.0 | How strong the colors are. |
| ColorMode → Distance → Brightness | Decimal | 1.0 | 0.0 to 1.0 | How bright the colors are. |
| ColorMode → Distance → Hue | Curve | | Distance 0 to 200, Hue 0 to 360 | Which color an entity gets at each distance. |
| ColorMode → Health → Alpha | Integer | 255 | 0 to 255 | How see-through arrows are when colored by health. |
| ColorMode → Static → Color | Color | | | One color for every arrow. |
| Alpha | Curve | | Distance 0 to 200, Alpha 0 to 1 | How see-through arrows are at each distance. Lower it for far distances to fade those arrows out. At 0 they are hidden. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleRadar.kt)*
