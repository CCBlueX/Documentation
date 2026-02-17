## HUD

Shows an in-game overlay with various useful tools.

**Category:** Render  
**Enabled by default:** Yes  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Blur (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── AlphaBlendRange (Decimal Range | default: 0.0..0.75 | range: 0.0..1.0)
├── SpaceSeperatedNames (Toggle | default: true)
├── Themes (Setting Group)
└── AdditionalComponents (Setting Group)
    └── Minimap (Toggleable Group | default: off)
        ├── Enabled (Toggle | default: false)
        ├── Alignment (Setting Group)
        │   ├── Horizontal (Choice | default: LEFT | options: Left, Center, CenterTranslated, Right)
        │   ├── HorizontalOffset (Integer | default: 7 | range: -1000..1000)
        │   ├── Vertical (Choice | default: TOP | options: Top, Center, CenterTranslated, Bottom)
        │   └── VerticalOffset (Integer | default: 180 | range: -1000..1000)
        ├── Size (Integer | default: 96 | range: 1..256)
        ├── ViewDistance (Decimal | default: 3.0 | range: 1.0..8.0)
        ├── FixedDirection (Toggle | default: false)
        ├── Texture (Toggleable Group | default: on)
        │   ├── Enabled (Toggle | default: true)
        │   └── VertexColor (Color)
        ├── Entity (Toggleable Group | default: on)
        │   ├── Enabled (Toggle | default: true)
        │   └── Scale (Decimal | default: 1.0 | range: 0.25..4.0)
        ├── Compass (Toggleable Group | default: off)
        │   ├── Enabled (Toggle | default: false)
        │   └── Placement (Choice | default: TOP_LEFT | options: TopLeft, TopRight, BottomLeft, BottomRight)
        └── Clock (Toggleable Group | default: off)
            ├── Enabled (Toggle | default: false)
            └── Placement (Choice | default: TOP_LEFT | options: TopLeft, TopRight, BottomLeft, BottomRight)
```

### Settings Details

#### Blur

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **AlphaBlendRange** (Decimal Range) — default: `0.0` – `0.75`; range: `0.0` – `1.0`

- **SpaceSeperatedNames** (Toggle) — default: `true`
#### Themes

A group of related settings.

#### AdditionalComponents

A group of related settings.

##### Minimap

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
###### Alignment

A group of related settings.

- **Horizontal** (Choice) — default: `LEFT`; options: `Left`, `Center`, `CenterTranslated`, `Right`
- **HorizontalOffset** (Integer) — default: `7`; range: `-1000` – `1000`
- **Vertical** (Choice) — default: `TOP`; options: `Top`, `Center`, `CenterTranslated`, `Bottom`
- **VerticalOffset** (Integer) — default: `180`; range: `-1000` – `1000`

- **Size** (Integer) — default: `96`; range: `1` – `256`
- **ViewDistance** (Decimal) — default: `3.0`; range: `1.0` – `8.0`
- **FixedDirection** (Toggle) — default: `false`
###### Texture

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **VertexColor** (Color)

###### Entity

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Scale** (Decimal) — default: `1.0`; range: `0.25` – `4.0`

###### Compass

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Placement** (Choice) — default: `TOP_LEFT`; options: `TopLeft`, `TopRight`, `BottomLeft`, `BottomRight`

###### Clock

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Placement** (Choice) — default: `TOP_LEFT`; options: `TopLeft`, `TopRight`, `BottomLeft`, `BottomRight`




### Screenshots

*Screenshots for HUD will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleHud.kt)*
