## LiquidFiller

Places blocks inside liquid source blocks within range of you, letting you quickly fill in water or lava around you. Optionally uses sponges to soak up water instead of placing solid blocks.

**Category:** World
**Enabled by default:** No

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── PlaceIn (Multi-Select | default: Water, Lava | options: Water, Lava)
├── PlaceOrder (Choice | default: FurtherFirst | options: Random, CloserFirst, FurtherFirst, BottomTop, TopBottom)
├── UseSponge (Toggle | default: false)
├── Filter (Choice | default: Whitelist | options: Whitelist, Blacklist)
├── Blocks (Block List)
└── Placer (Setting Group → see Shared: Block Placer)
```

### Settings Details

- **PlaceIn** (Multi-Select) — default: `Water`, `Lava`; options: `Water`, `Lava` — Which liquid types to fill. Cannot be empty.
- **PlaceOrder** (Choice) — default: `FurtherFirst`; options: `Random`, `CloserFirst`, `FurtherFirst`, `BottomTop`, `TopBottom` — Order in which liquid source blocks are queued for placing.
- **UseSponge** (Toggle) — default: `false` — Use a sponge on water sources to absorb nearby water with vanilla sponge behaviour instead of placing a solid block.
- **Filter** (Choice) — default: `Whitelist`; options: `Whitelist`, `Blacklist` — Whether the **Blocks** list is treated as the only blocks allowed (whitelist) or the only blocks forbidden (blacklist) for filling.
- **Blocks** (Block List) — The blocks used to fill liquids. Defaults to all wool colours plus dirt, cobblestone, stone, netherrack, diorite, granite, and andesite.

#### Placer

> The block placement settings (range, rotations, swing, delays, etc.) are the shared **Block Placer** group. See [Shared: Block Placer](/docs/modules/shared-settings/block-placer).

### Screenshots

*Screenshots for LiquidFiller will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2FModuleLiquidFiller.kt)*
