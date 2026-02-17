## HighJump

Allows you to jump higher.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Vanilla | modes: Vanilla, Vulcan)
│   └── [Mode: Vulcan]
│       └── Glide (Toggle | default: false)
└── Motion (Decimal | default: 0.8 | range: 0.2..10.0)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Vanilla**, **Vulcan**. Default: **Vanilla**.

##### Mode: Vulcan

- **Glide** (Toggle) — default: `false` — Enables a slow glide descent after reaching peak height.

- **Motion** (Decimal) — default: `0.8`; range: `0.2` – `10.0` — Upward jump motion applied when jumping.

### Screenshots

*Screenshots for HighJump will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleHighJump.kt)*
