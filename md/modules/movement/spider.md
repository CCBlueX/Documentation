## Spider

Allows you to climb walls like spiderman.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: Vanilla | modes: Vanilla, Polar-29.03.2025, Vulcan288)
    ├── [Mode: Vanilla]
    │   └── Motion (Decimal | default: 0.3 | range: 0.05..0.8)
    ├── [Mode: Polar-29.03.2025]
    │   └── JumpHeight (Decimal | default: 0.55 | range: 0.42..0.6)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Vanilla**, **Polar-29.03.2025**, **Vulcan288**. Default: **Vanilla**.

##### Mode: Vanilla

- **Motion** (Decimal) — default: `0.3`; range: `0.05` – `0.8` — Upward motion applied each tick when colliding with a wall.

##### Mode: Polar-29.03.2025

- **JumpHeight** (Decimal) — default: `0.55`; range: `0.42` – `0.6` — Jump height used when colliding with a wall to climb blocks.


### Screenshots

*Screenshots for Spider will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2Fspider%2FModuleSpider.kt)*
