## Nametags

Improves the visibility of player's name tags and show additional information.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Text (Setting Group)
│   └── Parts (Multi-Select | default: [Distance, Ping, Name, Health, BotMark] | options: Distance, Ping, Name, Health, BotMark)
├── Equipment (Setting Group)
│   ├── Slots (Multi-Select | default: [Mainhand, Head, Chest, Legs, Feet, Offhand] | options: Mainhand, Offhand, Feet, Legs, Chest, Head, Body, Saddle)
│   ├── SkipEmptySlot (Toggle | default: true)
│   ├── ShowInfo (Toggle | default: true)
│   └── HighlightItemInUse (Toggleable Group | default: off)
│       ├── Enabled (Toggle | default: false)
│       ├── FillColor (Color)
│       └── OutlineColor (Color)
├── Enchantment (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── Slots (Multi-Select | default: [Mainhand, Offhand, Head, Chest, Legs, Feet] | options: Mainhand, Offhand, Feet, Legs, Chest, Head, Body, Saddle)
├── Border (Toggle | default: true)
└── Scale (Curve)
```

### Settings Details

#### Text

A group of related settings.

- **Parts** (Multi-Select) — default: `Distance`, `Ping`, `Name`, `Health`, `BotMark`; options: `Distance`, `Ping`, `Name`, `Health`, `BotMark` — Components displayed in the name tag text.

#### Equipment

A group of related settings.

- **Slots** (Multi-Select) — default: `Mainhand`, `Head`, `Chest`, `Legs`, `Feet`, `Offhand`; options: `Mainhand`, `Offhand`, `Feet`, `Legs`, `Chest`, `Head`, `Body`, `Saddle` — Equipment slots shown above the name tag.
- **SkipEmptySlot** (Toggle) — default: `true` — Hides empty equipment slots from the display.
- **ShowInfo** (Toggle) — default: `true` — Shows durability and stack count on equipment items.
##### HighlightItemInUse

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Toggles highlighting the item currently in use.
- **FillColor** (Color) — Fill color of the in-use item highlight.
- **OutlineColor** (Color) — Outline color of the in-use item highlight.


#### Enchantment

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Toggles enchantment display below the name tag.
- **Slots** (Multi-Select) — default: `Mainhand`, `Offhand`, `Head`, `Chest`, `Legs`, `Feet`; options: `Mainhand`, `Offhand`, `Feet`, `Legs`, `Chest`, `Head`, `Body`, `Saddle` — Equipment slots whose enchantments are shown.

- **Border** (Toggle) — default: `true` — Draws a border around the name tag background.
- **Scale** (Curve) — Curve mapping distance to name tag display scale.

### Screenshots

*Screenshots for Nametags will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2Fnametags%2FModuleNametags.kt)*
