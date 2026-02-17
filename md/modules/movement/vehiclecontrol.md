## VehicleControl

Allows you to fly and speed while riding an entity (like boats or horses).

**Category:** Movement  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Glide (Decimal | default: -0.15 | range: -0.3..0.3)
├── MouseControl (Toggle | default: false)
├── NoGlideOnSpring (Toggle | default: false)
├── BaseSpeed (Setting Group)
│   ├── Horizontal (Decimal | default: 0.5 | range: 0.1..10.0)
│   └── Vertical (Decimal | default: 0.35 | range: 0.1..10.0)
├── SprintSpeed (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Horizontal (Decimal | default: 5.0 | range: 0.1..10.0)
│   └── Vertical (Decimal | default: 2.0 | range: 0.1..10.0)
└── Rehook (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── UnhookAfter (Integer | default: 4 | range: 1..10)
    └── HookAfter (Integer | default: 2 | range: 1..10)
```

### Settings Details

- **Glide** (Decimal) — default: `-0.15`; range: `-0.3` – `0.3` — Vertical drift speed when no vertical input is given and not in water.
- **MouseControl** (Toggle) — default: `false` — Steers the vehicle using the player's mouse direction.
- **NoGlideOnSpring** (Toggle) — default: `false` — Disables vertical glide when sprinting.
#### BaseSpeed

A group of related settings.

- **Horizontal** (Decimal) — default: `0.5`; range: `0.1` – `10.0` — Base horizontal movement speed for the vehicle.
- **Vertical** (Decimal) — default: `0.35`; range: `0.1` – `10.0` — Base vertical movement speed for the vehicle.

#### SprintSpeed

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles faster vehicle speed when sprint key is held.
- **Horizontal** (Decimal) — default: `5.0`; range: `0.1` – `10.0` — Horizontal speed when sprinting in a vehicle.
- **Vertical** (Decimal) — default: `2.0`; range: `0.1` – `10.0` — Vertical speed when sprinting in a vehicle.

#### Rehook

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles automatic re-hooking to bypass anti-cheat detection.
- **UnhookAfter** (Integer) — default: `4`; range: `1` – `10` — Ticks to wait before unhooking from the vehicle.
- **HookAfter** (Integer) — default: `2`; range: `1` – `10` — Ticks to wait before re-hooking to the vehicle.


### Screenshots

*Screenshots for VehicleControl will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmovement%2FModuleVehicleControl.kt)*
