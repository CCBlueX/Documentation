## CustomAmbience

Allows you to override the world ambience.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Weather (Choice | default: SNOWY | options: NoChange, Sunny, Rainy, Snowy, Thunder)
├── Time (Choice | default: NIGHT | options: NoChange, Dawn, Day, Noon, Dusk, Night, MidNight)
├── ModifyPrecipitation (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Gradient (Decimal | default: 0.7 | range: 0.1..1.0)
├── Fog (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── DisableWorldFog (Toggle | default: false)
│   ├── BackgroundColor (Color)
│   ├── Environmental (Decimal Range | default: 0.0..1024.0 | range: -16.0..2048.0)
│   ├── RenderDistance (Decimal Range | default: 230.0..256.0 | range: 0.0..1024.0)
│   ├── SkyEnd (Decimal | default: 256.0 | range: 0.0..1024.0)
│   └── CloudEnd (Decimal | default: 20480.0 | range: 0.0..4096.0)
├── CustomLightmap (Toggleable Group | default: off)
│   ├── Enabled (Toggle | default: false)
│   └── Color (Color)
└── SkyColor (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    └── Color (Color)
```

### Settings Details

- **Weather** (Choice) — default: `SNOWY`; options: `NoChange`, `Sunny`, `Rainy`, `Snowy`, `Thunder` — Overrides the current weather type.
- **Time** (Choice) — default: `NIGHT`; options: `NoChange`, `Dawn`, `Day`, `Noon`, `Dusk`, `Night`, `MidNight` — Overrides the time of day.
#### ModifyPrecipitation

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables precipitation intensity modification.
- **Gradient** (Decimal) — default: `0.7`; range: `0.1` – `1.0` — Controls the precipitation gradient intensity.

#### Fog

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables custom fog settings.
- **DisableWorldFog** (Toggle) — default: `false` — Disables the vanilla world fog entirely.
- **BackgroundColor** (Color) — Background clear color when fog is active.
- **Environmental** (Decimal Range) — default: `0.0` – `1024.0`; range: `-16.0` – `2048.0` — Start and end distances for environmental fog.
- **RenderDistance** (Decimal Range) — default: `230.0` – `256.0`; range: `0.0` – `1024.0` — Start and end distances for render distance fog.
- **SkyEnd** (Decimal) — default: `256.0`; range: `0.0` – `1024.0` — End distance for sky fog.
- **CloudEnd** (Decimal) — default: `20480.0`; range: `0.0` – `4096.0` — End distance for cloud fog.

#### CustomLightmap

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Enables a custom lightmap color overlay.
- **Color** (Color) — Color used for the custom lightmap.

#### SkyColor

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Enables a custom sky color override.
- **Color** (Color) — Color used for the sky.


### Screenshots

*Screenshots for CustomAmbience will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleCustomAmbience.kt)*
