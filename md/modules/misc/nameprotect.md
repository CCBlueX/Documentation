## NameProtect

Hides the player's real username client-side (useful for videos).

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Replacement (Text)
├── ColorMode (Mode Selector | default: Static | modes: Static, Rainbow)
│   ├── [Mode: Static]
│   │   └── Color (Color)
├── ObfuscateFriends (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── ColorMode (Mode Selector | default: Static | modes: Static, Rainbow)
│       ├── [Mode: Static]
│       │   └── Color (Color)
└── ObfuscateOthers (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    └── ColorMode (Mode Selector | default: Static | modes: Static, Rainbow)
        ├── [Mode: Static]
        │   └── Color (Color)
```

### Settings Details

- **Replacement** (Text)
#### ColorMode

Select a mode for this feature. Available modes: **Static**, **Rainbow**. Default: **Static**.

##### Mode: Static

- **Color** (Color)

#### ObfuscateFriends

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### ColorMode

Select a mode for this feature. Available modes: **Static**, **Rainbow**. Default: **Static**.

###### Mode: Static

- **Color** (Color)


#### ObfuscateOthers

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
##### ColorMode

Select a mode for this feature. Available modes: **Static**, **Rainbow**. Default: **Static**.

###### Mode: Static

- **Color** (Color)



### Screenshots

*Screenshots for NameProtect will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleNameProtect.kt)*
