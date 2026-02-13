## Notebot

Automatically plays note block songs from NBS (Note Block Song) file.

**Category:** Fun  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Song (File)
├── PianoOnly (Toggle | default: false)
├── ReuseBlocks (Toggle | default: true)
├── Range (Decimal | default: 6.0 | range: 1.0..6.0)
├── IgnoreOpenInventory (Toggle | default: true)
├── StartDelay (Setting Group)
│   ├── Test (Integer | default: 0 | range: 0..20 | ticks)
│   ├── Tune (Integer | default: 0 | range: 0..20 | ticks)
│   └── Play (Integer | default: 2 | range: 0..20 | ticks)
└── Render (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── Clump (Toggle | default: true)
    ├── StartSize (Decimal | default: 1.0 | range: 0.0..2.0)
    ├── StartCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── EndSize (Decimal | default: 0.8 | range: 0.0..2.0)
    ├── EndCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── FadeInCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── FadeOutCurve (Choice | default: LINEAR | options: Linear, QuadIn, QuadOut, QuadInOut, ExponentialIn, ExponentialOut, None)
    ├── InTime (Integer | default: 500 | range: 0..5000 | ms)
    ├── OutTime (Integer | default: 500 | range: 0..5000 | ms)
    ├── Color (Color)
    ├── OutlineColor (Color)
    ├── TestColor (Color)
    ├── TestOutlineColor (Color)
    ├── TuneColor (Color)
    └── TuneOutlineColor (Color)
```

### Settings Details

- **Song** (File)
- **PianoOnly** (Toggle) — default: `false`
- **ReuseBlocks** (Toggle) — default: `true`
- **Range** (Decimal) — default: `6.0`; range: `1.0` – `6.0`
- **IgnoreOpenInventory** (Toggle) — default: `true`
#### StartDelay

A group of related settings.

- **Test** (Integer) — default: `0`; range: `0` – `20`; unit: ticks
- **Tune** (Integer) — default: `0`; range: `0` – `20`; unit: ticks
- **Play** (Integer) — default: `2`; range: `0` – `20`; unit: ticks

#### Render

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Clump** (Toggle) — default: `true`
- **StartSize** (Decimal) — default: `1.0`; range: `0.0` – `2.0`
- **StartCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **EndSize** (Decimal) — default: `0.8`; range: `0.0` – `2.0`
- **EndCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **FadeInCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **FadeOutCurve** (Choice) — default: `LINEAR`; options: `Linear`, `QuadIn`, `QuadOut`, `QuadInOut`, `ExponentialIn`, `ExponentialOut`, `None`
- **InTime** (Integer) — default: `500`; range: `0` – `5000`; unit: ms
- **OutTime** (Integer) — default: `500`; range: `0` – `5000`; unit: ms
- **Color** (Color)
- **OutlineColor** (Color)
- **TestColor** (Color)
- **TestOutlineColor** (Color)
- **TuneColor** (Color)
- **TuneOutlineColor** (Color)


### Screenshots

*Screenshots for Notebot will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Ffun%2FModuleNoteBot.kt)*
