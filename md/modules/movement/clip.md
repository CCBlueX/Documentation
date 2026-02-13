## Clip

Allows you to clip through blocks.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Choice (Mode Selector | default: Fancy | modes: Fancy, Old)
    ├── [Mode: Fancy]
    │   ├── Horizontal (Integer | default: 0 | range: 0..6)
    │   ├── Vertical (Integer | default: 5 | range: 0..6)
    │   └── RequiresStandOn (Toggle | default: true)
    └── [Mode: Old]
        ├── Horizontal (Decimal | default: 0.0 | range: -10.0..10.0)
        ├── Vertical (Decimal | default: 5.0 | range: -10.0..10.0)
        └── ResetVelocity (Toggle | default: true)
```

### Settings Details

#### Choice

Select a mode for this feature. Available modes: **Fancy**, **Old**. Default: **Fancy**.

##### Mode: Fancy

- **Horizontal** (Integer) — default: `0`; range: `0` – `6` — Number of blocks to search horizontally when clipping through walls.
- **Vertical** (Integer) — default: `5`; range: `0` – `6` — Number of blocks to search vertically when clipping through floors or ceilings.
- **RequiresStandOn** (Toggle) — default: `true` — Requires a solid block below the destination to clip into.

##### Mode: Old

- **Horizontal** (Decimal) — default: `0.0`; range: `-10.0` – `10.0` — Distance to teleport in the direction you are facing.
- **Vertical** (Decimal) — default: `5.0`; range: `-10.0` – `10.0` — Distance to teleport vertically.
- **ResetVelocity** (Toggle) — default: `true` — Resets your velocity to zero after clipping.


### Screenshots

*Screenshots for Clip will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleClip.kt)*
