## Derp

Makes it look as if you were derping around to other players

**Category:** Fun  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Yaw (Mode Selector | default: Random | modes: Static, Offset, Random, Jitter, Spin)
│   ├── [Mode: Static]
│   │   └── Yaw (Decimal | default: 0.0 | range: -180.0..180.0 | °)
│   ├── [Mode: Offset]
│   │   └── Offset (Decimal | default: 0.0 | range: -180.0..180.0 | °)
│   ├── [Mode: Jitter]
│   │   ├── ForwardTicks (Integer | default: 2 | range: 0..100 | ticks)
│   │   └── BackwardTicks (Integer | default: 2 | range: 0..100 | ticks)
│   └── [Mode: Spin]
│       └── Speed (Integer | default: 50 | range: -70..70 | °/tick)
├── Pitch (Mode Selector | default: Random | modes: Static, Offset, Random)
│   ├── [Mode: Static]
│   │   └── Pitch (Decimal | default: -90.0 | range: -180.0..180.0 | °)
│   ├── [Mode: Offset]
│   │   └── Offset (Decimal | default: 0.0 | range: -180.0..180.0 | °)
├── SafePitch (Toggle | default: true)
└── NotDuringSprint (Toggle | default: true)
```

### Settings Details

#### Yaw

Select a mode for this feature. Available modes: **Static**, **Offset**, **Random**, **Jitter**, **Spin**. Default: **Random**.

##### Mode: Static

- **Yaw** (Decimal) — default: `0.0`; range: `-180.0` – `180.0`; unit: °

##### Mode: Offset

- **Offset** (Decimal) — default: `0.0`; range: `-180.0` – `180.0`; unit: °

##### Mode: Jitter

- **ForwardTicks** (Integer) — default: `2`; range: `0` – `100`; unit: ticks
- **BackwardTicks** (Integer) — default: `2`; range: `0` – `100`; unit: ticks

##### Mode: Spin

- **Speed** (Integer) — default: `50`; range: `-70` – `70`; unit: °/tick

#### Pitch

Select a mode for this feature. Available modes: **Static**, **Offset**, **Random**. Default: **Random**.

##### Mode: Static

- **Pitch** (Decimal) — default: `-90.0`; range: `-180.0` – `180.0`; unit: °

##### Mode: Offset

- **Offset** (Decimal) — default: `0.0`; range: `-180.0` – `180.0`; unit: °

- **SafePitch** (Toggle) — default: `true`
- **NotDuringSprint** (Toggle) — default: `true`

### Screenshots

*Screenshots for Derp will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Ffun%2FModuleDerp.kt)*
