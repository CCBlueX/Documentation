## AntiVoid

Protects you from falling into the void.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: GhostBlock | modes: GhostBlock, Flag, Blink)
│   ├── [Mode: Flag]
│   │   ├── FallDistance (Decimal | default: 0.5 | range: 0.0..6.0)
│   │   ├── Height (Decimal | default: 0.42 | range: 0.01..10.0)
│   │   └── Silent (Toggle | default: false)
└── VoidLevel (Integer | default: 0 | range: -256..0)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **GhostBlock**, **Flag**, **Blink**. Default: **GhostBlock**.

##### Mode: Flag

- **FallDistance** (Decimal) — default: `0.5`; range: `0.0` – `6.0` — Minimum fall distance before triggering the flag action.
- **Height** (Decimal) — default: `0.42`; range: `0.01` – `10.0` — Height to teleport the player upward when rescued.
- **Silent** (Toggle) — default: `false` — Adjusts position via network packets instead of moving the player visually.

- **VoidLevel** (Integer) — default: `0`; range: `-256` – `0` — The Y-level at which the void is deemed to begin.

### Screenshots

*Screenshots for AntiVoid will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2Fantivoid%2FModuleAntiVoid.kt)*
