## BedPlates

Allows you to see what blocks are around the bed

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── BackgroundColor (Color)
├── Outline (Toggle | default: false)
├── MaxLayers (Integer | default: 5 | range: 1..5)
├── ShowBed (Toggle | default: true)
├── TextShadow (Toggle | default: true)
├── RenderOffset (3D Position)
├── Scale (Curve)
├── MaxCount (Integer | default: 8 | range: 1..64)
├── HighlightUnbreakable (Toggle | default: true)
├── Compact (Toggle | default: true)
├── PreventOverlap (Toggle | default: true)
├── FilterMode (Mode Selector | default: Predefined | modes: Predefined, Custom)
│   └── [Mode: Custom]
│       ├── Blocks (Registry List)
│       └── Filter (Choice | default: BLACKLIST | options: Whitelist, Blacklist)
├── IgnoreSelfBed (Mode Selector | default: None | modes: None, Color, SpawnLocation, Manual)
│   ├── [Mode: Color]
│   │   └── Slots (Multi-Select | default: [Head] | options: Feet, Legs, Chest, Head)
│   ├── [Mode: SpawnLocation]
│   │   └── BedDistance (Decimal | default: 24.0 | range: 16.0..48.0)
│   └── [Mode: Manual]
│       ├── Track (Key)
│       └── Untrack (Key)
└── IgnoreAdjacent (Toggle | default: false)
```

### Settings Details

- **BackgroundColor** (Color) — Sets the background color behind the bed plate display.
- **Outline** (Toggle) — default: `false` — Draws an outline colored by the bed's map color.
- **MaxLayers** (Integer) — default: `5`; range: `1` – `5` — Maximum number of surrounding block layers to scan around each bed.
- **ShowBed** (Toggle) — default: `true` — Includes the bed itself as the first item in the plate display.
- **TextShadow** (Toggle) — default: `true` — Enables text shadow on item count and layer labels.
- **RenderOffset** (3D Position) — Adjusts the 3D position offset of the bed plate overlay.
- **Scale** (Curve) — Controls how the plate scales based on distance from the camera.
- **MaxCount** (Integer) — default: `8`; range: `1` – `64` — Maximum number of bed plates to render at once.
- **HighlightUnbreakable** (Toggle) — default: `true` — Highlights blocks in red if you lack the correct tool to break them.
- **Compact** (Toggle) — default: `true` — Combines duplicate surrounding blocks into a single entry with a count.
- **PreventOverlap** (Toggle) — default: `true` — Prevents bed plate overlays from overlapping each other.
#### FilterMode

Select a mode for this feature. Available modes: **Predefined**, **Custom**. Default: **Predefined**.

##### Mode: Custom

- **Blocks** (Registry List) — Registry list of blocks for the custom filter.
- **Filter** (Choice) — default: `BLACKLIST`; options: `Whitelist`, `Blacklist` — Choose whitelist or blacklist for the custom block filter.

#### IgnoreSelfBed

Select a mode for this feature. Available modes: **None**, **Color**, **SpawnLocation**, **Manual**. Default: **None**.

##### Mode: Color

- **Slots** (Multi-Select) — default: `Head`; options: `Feet`, `Legs`, `Chest`, `Head` — Armor slots to check for bed color matching.

##### Mode: SpawnLocation

- **BedDistance** (Decimal) — default: `24.0`; range: `16.0` – `48.0` — Maximum distance from spawn to consider a bed as yours.

##### Mode: Manual

- **Track** (Key) — Key bind to mark a bed as your own.
- **Untrack** (Key) — Key bind to remove a bed from your tracked list.

- **IgnoreAdjacent** (Toggle) — default: `false` — Skips rendering bed plates for beds adjacent to other tracked beds.

### Screenshots

*Screenshots for BedPlates will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleBedPlates.kt)*
