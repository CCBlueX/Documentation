## VoidESP

VoidESP highlights the floor positions around you that have no solid ground beneath them — marking spots where a misstep would send you straight into the void. It scans a rectangular area centered on your current location every tick and draws a coloured overlay on any surface block that lacks a sturdy floor within the configured depth below it. This makes it easy to spot dangerous gaps on sky-island maps, void-bridges, end platforms, or Crystal PvP arenas without having to stare at your feet.

The scan area is shaped relative to the direction you are facing: **RangeFacing** controls how far ahead and behind you the module looks, while **RangeSide** controls how wide that rectangle extends to your left and right. **YThreshold** determines how far down the module searches for a solid floor before concluding that a spot is void. Increasing these values gives you more warning distance at the cost of slightly more work per tick; tightening them keeps the overlay focused on the immediate danger zone directly ahead.

For automatic protection against falling into the void, pair this module with [AntiVoid](/docs/modules/player/antivoid), which will act as a safety net even if you miss a highlighted tile.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| YThreshold | Integer | 16 | 3–32 | How many blocks downward the module searches below each scanned position for a solid floor. If no sturdy surface is found within this depth, the position is marked as void. |
| RangeSide | Integer | 3 | 0–32 | How many blocks to the left and right of your facing direction are included in the scan area. |
| RangeFacing | Integer | 8 | 1–32 | How many blocks in front of and behind you are included in the scan area. |
| Render | Toggleable Group | on | — | See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleVoidESP.kt)*
