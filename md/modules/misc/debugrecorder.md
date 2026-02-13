## DebugRecorder

Only of interest to developers.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Mode (Mode Selector | default: Generic | modes: Combat, CombatTrainer, Generic, CPS, Aim, Box)
    ├── [Mode: Combat]
    │   └── Target (Setting Group)
    │       ├── Range (Decimal | default: 10.0 | range: 7.0..12.0)
    │       ├── FOV (Decimal | default: 180.0 | range: 0.0..180.0)
    │       ├── HurtTime (Integer | default: 10 | range: 0..10)
    │       └── Priority (Multi-Select | default: [Type, Direction] | options: Type, Health, Distance, Direction, HurtTime, Age)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Combat**, **CombatTrainer**, **Generic**, **CPS**, **Aim**, **Box**. Default: **Generic**.

##### Mode: Combat

###### Target

A group of related settings.

- **Range** (Decimal) — default: `10.0`; range: `7.0` – `12.0`
- **FOV** (Decimal) — default: `180.0`; range: `0.0` – `180.0`
- **HurtTime** (Integer) — default: `10`; range: `0` – `10`
- **Priority** (Multi-Select) — default: `Type`, `Direction`; options: `Type`, `Health`, `Distance`, `Direction`, `HurtTime`, `Age`



### Screenshots

*Screenshots for DebugRecorder will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleDebugRecorder.kt)*
