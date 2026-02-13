## Freeze

Allows you to freeze yourself in your current position without the server knowing.

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Stationary | modes: Queue, Cancel, Stationary)
│   ├── [Mode: Queue]
│   │   └── Origin (Multi-Select | default: [Outgoing] | options: Incoming, Outgoing)
│   ├── [Mode: Cancel]
│   │   └── Origin (Multi-Select | default: [Outgoing] | options: Incoming, Outgoing)
│   └── [Mode: Stationary]
│       └── CancelC0B (Toggle | default: true)
├── DisableOnFlag (Toggle | default: true)
├── Notification (Toggle | default: false)
└── BalanceWarp (Toggle | default: false)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Queue**, **Cancel**, **Stationary**. Default: **Stationary**.

##### Mode: Queue

- **Origin** (Multi-Select) — default: `Outgoing`; options: `Incoming`, `Outgoing` — Which packet directions to queue (delay) while frozen.

##### Mode: Cancel

- **Origin** (Multi-Select) — default: `Outgoing`; options: `Incoming`, `Outgoing` — Which packet directions to cancel while frozen.

##### Mode: Stationary

- **CancelC0B** (Toggle) — default: `true` — Cancels pong packets to bypass timer checks from anti-cheats like Grim.

- **DisableOnFlag** (Toggle) — default: `true` — Disables the module when the server sends a position correction.
- **Notification** (Toggle) — default: `false` — Shows a notification when the module is disabled due to a flag.
- **BalanceWarp** (Toggle) — default: `false` — Replays all missed ticks when disabled to catch up to server state.

### Screenshots

*Screenshots for Freeze will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleFreeze.kt)*
