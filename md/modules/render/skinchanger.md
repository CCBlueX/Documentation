## SkinChanger

Hides the player's real skin client-side (useful for videos).

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── ForceOverride (Toggle | default: false)
├── UploadSkin (Toggle | default: false)
└── Mode (Mode Selector | default: Online | modes: Online, File)
    ├── [Mode: Online]
    │   └── Username (Text)
    └── [Mode: File]
        ├── Image (File)
        └── Model (Choice | default: WIDE | options: Slim, Default)
```

### Settings Details

- **ForceOverride** (Toggle) — default: `false` — Forces the skin override via mixin even when the player list entry is unreliable.
- **UploadSkin** (Toggle) — default: `false` — Uploads the selected skin to your Mojang account.
#### Mode

Select a mode for this feature. Available modes: **Online**, **File**. Default: **Online**.

##### Mode: Online

- **Username** (Text) — Sets the player username to fetch the skin from.

##### Mode: File

- **Image** (File) — Selects a local image file to use as the skin texture.
- **Model** (Choice) — default: `WIDE`; options: `Slim`, `Default` — Selects the player model type (slim or wide).


### Screenshots

*Screenshots for SkinChanger will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleSkinChanger.kt)*
