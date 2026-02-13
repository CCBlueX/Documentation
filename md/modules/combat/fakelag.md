## FakeLag

Holds back packets so as to prevent you from being hit by an enemy.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Range (Decimal Range | default: 2.0..5.0 | range: 0.0..10.0)
├── Delay (Integer Range | default: 300..600 | range: 0..1000 | ms)
├── RecoilTime (Integer | default: 250 | range: 0..1000 | ms)
├── Mode (Choice | default: DYNAMIC | options: Constant, Dynamic)
└── FlushOn (Multi-Select | default: [EntityInteract, BlockInteract, Action] | options: EntityInteract, BlockInteract, Action)
```

### Settings Details

- **Range** (Decimal Range) — default: `2.0` – `5.0`; range: `0.0` – `10.0` — Distance range to an enemy required for packet holding to activate.
- **Delay** (Integer Range) — default: `300` – `600`; range: `0` – `1000`; unit: ms — How long outgoing packets are held back.
- **RecoilTime** (Integer) — default: `250`; range: `0` – `1000`; unit: ms — Minimum time after a flush before lagging resumes.
- **Mode** (Choice) — default: `DYNAMIC`; options: `Constant`, `Dynamic` — Constant always lags; Dynamic only lags when the server position is farther from enemies than the client position.
- **FlushOn** (Multi-Select) — default: `EntityInteract`, `BlockInteract`, `Action`; options: `EntityInteract`, `BlockInteract`, `Action` — Packet types that immediately flush all queued packets.

### Screenshots

*Screenshots for FakeLag will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleFakeLag.kt)*
