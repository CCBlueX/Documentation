## FlagCheck

Alerts you about flags.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── ChatMessage (Toggle | default: true)
├── Notification (Toggle | default: false)
├── InvalidAttributes (Toggle | default: false)
├── ResetFlags (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── After (Integer | default: 30 | range: 1..300 | s)
└── Render (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── NotInFirstPerson (Toggle | default: true)
    ├── Alive (Integer | default: 1000 | range: 0..3000 | ms)
    ├── FadeOut (Choice | default: QUAD_OUT | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── OutTime (Integer | default: 500 | range: 0..2000 | ms)
    ├── Color (Color)
    └── OutlineColor (Color)
```

### Settings Details

- **ChatMessage** (Toggle) — default: `true`
- **Notification** (Toggle) — default: `false`
- **InvalidAttributes** (Toggle) — default: `false`
#### ResetFlags

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **After** (Integer) — default: `30`; range: `1` – `300`; unit: s

#### Render

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **NotInFirstPerson** (Toggle) — default: `true`
- **Alive** (Integer) — default: `1000`; range: `0` – `3000`; unit: ms
- **FadeOut** (Choice) — default: `QUAD_OUT`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **OutTime** (Integer) — default: `500`; range: `0` – `2000`; unit: ms
- **Color** (Color)
- **OutlineColor** (Color)


### Screenshots

*Screenshots for FlagCheck will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleFlagCheck.kt)*
