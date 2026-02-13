## BetterInventory

Additional inventory-related visual features.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── HighlightClicked (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Mode (Mode Selector | default: Border | modes: Border, Texture)
│       ├── [Mode: Border]
│       │   └── Color (Color)
├── TextCooldownProgress (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Mode (Choice | default: PERCENTAGE | options: Percentage, DurationTicks, DurationSeconds)
│   ├── Scale (Decimal | default: 1.0 | range: 0.25..4.0)
│   └── Color (Color)
└── ContainerItemView (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── SkipEmptyStack (Toggle | default: false)
    ├── Scale (Decimal | default: 1.0 | range: 0.25..4.0)
    ├── RelativeToMouse (Toggle | default: true)
    ├── RenderOffsetX (Decimal | default: 150.0 | range: -4096.0..4096.0)
    └── RenderOffsetY (Decimal | default: 0.0 | range: -4096.0..4096.0)
```

### Settings Details

#### HighlightClicked

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables highlighting of the last clicked inventory slot.
##### Mode

Select a mode for this feature. Available modes: **Border**, **Texture**. Default: **Border**.

###### Mode: Border

- **Color** (Color) — Color of the border highlight around the clicked slot.


#### TextCooldownProgress

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables displaying cooldown progress as text over items.
- **Mode** (Choice) — default: `PERCENTAGE`; options: `Percentage`, `DurationTicks`, `DurationSeconds` — Format for displaying cooldown progress.
- **Scale** (Decimal) — default: `1.0`; range: `0.25` – `4.0` — Scale of the cooldown progress text.
- **Color** (Color) — Color of the cooldown progress text.

#### ContainerItemView

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables the container content preview on hover.
- **SkipEmptyStack** (Toggle) — default: `false` — Hides empty item slots in the container preview.
- **Scale** (Decimal) — default: `1.0`; range: `0.25` – `4.0` — Scale of the container preview display.
- **RelativeToMouse** (Toggle) — default: `true` — Positions the preview relative to the mouse cursor.
- **RenderOffsetX** (Decimal) — default: `150.0`; range: `-4096.0` – `4096.0` — Horizontal offset of the container preview.
- **RenderOffsetY** (Decimal) — default: `0.0`; range: `-4096.0` – `4096.0` — Vertical offset of the container preview.


### Screenshots

*Screenshots for BetterInventory will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleBetterInventory.kt)*
