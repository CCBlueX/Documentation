## Nametags

Improves the visibility of player name tags and shows additional information.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Text (Setting Group)
│   └── Parts (Multi-Select | default: [Distance, Ping, Name, Health, GameMode, BotMark] | options: Distance, Ping, Name, Health, GameMode, BotMark)
├── Equipment (Setting Group)
│   ├── Slots (Multi-Select | default: [Mainhand, Head, Chest, Legs, Feet, Offhand] | options: Mainhand, Offhand, Feet, Legs, Chest, Head, Body, Saddle)
│   ├── SkipEmptySlot (Toggle | default: true)
│   ├── ShowInfo (Toggle | default: true)
│   ├── Enchantment (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   ├── Scale (Decimal | default: 0.8 | range: 0.25..4.0)
│   │   ├── MaxCountPerItem (Integer | default: 4 | range: 1..16)
│   │   └── BackgroundRadius (Decimal | default: 1.0 | range: 0.0..8.0)
│   └── HighlightItemInUse (Toggleable Group | default: off)
│       ├── Enabled (Toggle | default: false)
│       ├── FillColor (Color)
│       └── OutlineColor (Color)
├── BorderWidth (Decimal | default: 1.0 | range: 0.0..8.0)
├── BackgroundRadius (Decimal | default: 2.0 | range: 0.0..16.0)
└── Scale (Curve)
```

### Settings Details

#### Text

A group of related settings.

- **Parts** (Multi-Select) — default: `Distance`, `Ping`, `Name`, `Health`, `GameMode`, `BotMark`; options: `Distance`, `Ping`, `Name`, `Health`, `GameMode`, `BotMark` — Components displayed in the name tag text. `GameMode` shows the player's current game mode.

#### Equipment

A group of related settings.

- **Slots** (Multi-Select) — default: `Mainhand`, `Head`, `Chest`, `Legs`, `Feet`, `Offhand`; options: `Mainhand`, `Offhand`, `Feet`, `Legs`, `Chest`, `Head`, `Body`, `Saddle` — Equipment slots shown above the name tag.
- **SkipEmptySlot** (Toggle) — default: `true` — Hides empty equipment slots from the display.
- **ShowInfo** (Toggle) — default: `true` — Shows durability and stack count on equipment items.
##### Enchantment

A toggleable group of settings (default: enabled). Shows the enchantments of the displayed equipment.

- **Enabled** (Toggle) — default: `true`
- **Scale** (Decimal) — default: `0.8`; range: `0.25` – `4.0` — Size of the enchantment text relative to the name tag.
- **MaxCountPerItem** (Integer) — default: `4`; range: `1` – `16` — Maximum number of enchantments shown per item before the rest are summarized.
- **BackgroundRadius** (Decimal) — default: `1.0`; range: `0.0` – `8.0` — Corner rounding of the enchantment background.

##### HighlightItemInUse

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false` — Highlights the item the player is currently using.
- **FillColor** (Color) — Fill color of the in-use item highlight.
- **OutlineColor** (Color) — Outline color of the in-use item highlight.

- **BorderWidth** (Decimal) — default: `1.0`; range: `0.0` – `8.0` — Thickness of the border drawn around the name tag background (0 disables it).
- **BackgroundRadius** (Decimal) — default: `2.0`; range: `0.0` – `16.0` — Corner rounding of the name tag background.
- **Scale** (Curve) — Curve mapping camera distance to name tag display scale.

### Screenshots

*Screenshots for Nametags will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2Fnametags%2FModuleNametags.kt)*
