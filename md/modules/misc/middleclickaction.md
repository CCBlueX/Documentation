## MiddleClickAction

Allows you to perform actions with middle clicks.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: FriendClicker | modes: FriendClicker, Pearl)
    ├── [Mode: FriendClicker]
    │   └── PickUpRange (Decimal | default: 3.0 | range: 1.0..100.0)
    └── [Mode: Pearl]
        ├── SlotResetDelay (Integer | default: 1 | range: 0..10 | ticks)
        └── StopOnSubmit (Decimal Range | default: 85.0..90.0 | range: 60.0..90.0 | Pitch)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **FriendClicker**, **Pearl**. Default: **FriendClicker**.

##### Mode: FriendClicker

- **PickUpRange** (Decimal) — default: `3.0`; range: `1.0` – `100.0`

##### Mode: Pearl

- **SlotResetDelay** (Integer) — default: `1`; range: `0` – `10`; unit: ticks
- **StopOnSubmit** (Decimal Range) — default: `85.0` – `90.0`; range: `60.0` – `90.0`; unit: Pitch


### Screenshots

*Screenshots for MiddleClickAction will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleMiddleClickAction.kt)*
