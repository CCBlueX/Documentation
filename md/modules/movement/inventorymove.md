## InventoryMove

Allows you to walk while an inventory is opened.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Behavior (Choice | default: NORMAL | options: Normal, Safe, Undetectable, StopOnAction)
├── PassthroughSneak (Toggle | default: false)
├── SprintControl (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   ├── Client (Choice | default: DO_NOT_CHANGE | options: DoNotChange, ForceSprint, ForceNoSprint)
│   └── Server (Choice | default: DO_NOT_CHANGE | options: DoNotChange, ForceSprint, ForceNoSprint)
├── SneakControl (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   └── Client (Choice | default: DO_NOT_CHANGE | options: DoNotChange, ForceSneak, ForceNoSneak)
├── Timer (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   └── Speed (Decimal | default: 1.0 | range: 0.1..2.0)
└── Blink (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    └── MaximumTime (Integer | default: 10000 | range: 0..30000 | ms)
```

### Settings Details

- **Behavior** (Choice) — default: `NORMAL`; options: `Normal`, `Safe`, `Undetectable`, `StopOnAction`
- **PassthroughSneak** (Toggle) — default: `false`
#### SprintControl

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Client** (Choice) — default: `DO_NOT_CHANGE`; options: `DoNotChange`, `ForceSprint`, `ForceNoSprint`
- **Server** (Choice) — default: `DO_NOT_CHANGE`; options: `DoNotChange`, `ForceSprint`, `ForceNoSprint`

#### SneakControl

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Client** (Choice) — default: `DO_NOT_CHANGE`; options: `DoNotChange`, `ForceSneak`, `ForceNoSneak`

#### Timer

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Speed** (Decimal) — default: `1.0`; range: `0.1` – `2.0`

#### Blink

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **MaximumTime** (Integer) — default: `10000`; range: `0` – `30000`; unit: ms


### Screenshots

*Screenshots for InventoryMove will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleInventoryMove.kt)*
