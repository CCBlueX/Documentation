## FreeLook

Allows you to move the camera freely around your character.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Perspective (Choice | default: BACK | options: Front, Back)
├── SenseBoost (Decimal | default: 1.0 | range: 0.1..2.0)
└── NoPitchLimit (Toggle | default: true)
```

### Settings Details

- **Perspective** (Choice) — default: `BACK`; options: `Front`, `Back` — Camera perspective to use when free looking.
- **SenseBoost** (Decimal) — default: `1.0`; range: `0.1` – `2.0` — Multiplier for mouse sensitivity while free looking.
- **NoPitchLimit** (Toggle) — default: `true` — Removes the ±90° pitch clamp for the camera.

### Screenshots

*Screenshots for FreeLook will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleFreeLook.kt)*
