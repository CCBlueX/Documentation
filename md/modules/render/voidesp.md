## VoidESP

VoidESP marks the spots around you where there is no ground below, so you can see where you would fall into the void. It helps on sky island and bridge maps. [AntiVoid](/docs/modules/player/antivoid) can save you if you fall anyway.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| YThreshold | Integer | 16 | 3 to 32 | How many blocks down to look for ground. If there is none, the spot is marked. |
| RangeSide | Integer | 3 | 0 to 32 | How many blocks to your left and right are checked. |
| RangeFacing | Integer | 8 | 1 to 32 | How many blocks in front of and behind you are checked. |
| Render | Toggleable Group | on | | How the marked spots look. See [Shared: Placement Rendering](/docs/modules/shared-settings/placement-rendering). |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleVoidESP.kt)*
