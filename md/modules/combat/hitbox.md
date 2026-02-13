## Hitbox

Enlarges the hit box of targets.

**Category:** Combat  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Size (Decimal | default: 0.1 | range: 0.0..1.0)
├── ApplyToDebugHitbox (Toggle | default: true)
└── ApplyToComponent (Toggle | default: true)
```

### Settings Details

- **Size** (Decimal) — default: `0.1`; range: `0.0` – `1.0` — Extra margin added to each attackable entity's hitbox.
- **ApplyToDebugHitbox** (Toggle) — default: `true` — Also enlarges the debug (F3+B) hitbox display.
- **ApplyToComponent** (Toggle) — default: `true` — Also applies the expansion to the item component attack-range hitbox margin.

### Screenshots

*Screenshots for Hitbox will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fcombat%2FModuleHitbox.kt)*
