## CameraClip

Allows you to clip the camera through walls in third person mode.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── CameraDistance (Decimal | default: 4.0 | range: 1.0..48.0)
├── Animation (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Speed (Decimal | default: 0.6 | range: 0.1..1.0)
└── ScrollAdjust (Toggleable Group | default: on)
    ├── Enabled (Toggle | default: true)
    ├── Modifier (Key)
    ├── Sensitivity (Decimal | default: 0.3 | range: 0.1..2.0)
    ├── RememberScrolled (Toggle | default: false)
    └── RequireFreeLook (Toggle | default: false)
```

### Settings Details

- **CameraDistance** (Decimal) — default: `4.0`; range: `1.0` – `48.0` — Distance of the third-person camera from the player.

#### Animation

A toggleable group of settings (default: enabled). Smoothly animates the camera moving in and out instead of snapping.

- **Enabled** (Toggle) — default: `true`
- **Speed** (Decimal) — default: `0.6`; range: `0.1` – `1.0` — How quickly the camera distance animates.

#### ScrollAdjust

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables scroll-wheel adjustment of the camera distance.
- **Modifier** (Key) — Key that must be held to scroll-adjust the camera distance.
- **Sensitivity** (Decimal) — default: `0.3`; range: `0.1` – `2.0` — How much each scroll step changes the distance.
- **RememberScrolled** (Toggle) — default: `false` — Saves the scrolled distance as the new default when releasing the modifier.
- **RequireFreeLook** (Toggle) — default: `false` — Only allows scroll adjustment while FreeLook is active.


### Screenshots

*Screenshots for CameraClip will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2Fcameraclip%2FModuleCameraClip.kt)*
