## StorageESP

Highlights all blocks that can contain items allowing you to see them rough walls.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Glow | modes: Box, Glow)
│   ├── [Mode: Box]
│   │   └── Outline (Toggle | default: true)
├── Chest (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Color (Color)
│   └── Tracers (Toggle | default: false)
├── EnderChest (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Color (Color)
│   └── Tracers (Toggle | default: false)
├── Furnace (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Color (Color)
│   └── Tracers (Toggle | default: false)
├── BrewingStand (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Color (Color)
│   └── Tracers (Toggle | default: false)
├── Dispenser (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Color (Color)
│   └── Tracers (Toggle | default: false)
├── Hopper (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Color (Color)
│   └── Tracers (Toggle | default: false)
├── ShulkerBox (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Color (Color)
│   └── Tracers (Toggle | default: false)
├── Pot (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Color (Color)
│   └── Tracers (Toggle | default: false)
├── Shelf (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Color (Color)
│   └── Tracers (Toggle | default: false)
├── RequiresChestStealer (Toggle | default: false)
└── DistanceFade (Setting Group)
    ├── NearStart (Decimal | default: 0.0 | range: 0.0..512.0)
    ├── NearEnd (Decimal | default: 0.0 | range: 0.0..512.0)
    ├── FarStart (Decimal | default: 512.0 | range: 0.0..512.0)
    └── FarEnd (Decimal | default: 512.0 | range: 0.0..512.0)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Box**, **Glow**. Default: **Glow**.

##### Mode: Box

- **Outline** (Toggle) — default: `true` — Draws outlines around storage container boxes.

#### Chest

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables highlighting for chests.
- **Color** (Color) — Sets the highlight color for chests.
- **Tracers** (Toggle) — default: `false` — Draws tracer lines to chests.

#### EnderChest

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables highlighting for ender chests.
- **Color** (Color) — Sets the highlight color for ender chests.
- **Tracers** (Toggle) — default: `false` — Draws tracer lines to ender chests.

#### Furnace

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables highlighting for furnaces.
- **Color** (Color) — Sets the highlight color for furnaces.
- **Tracers** (Toggle) — default: `false` — Draws tracer lines to furnaces.

#### BrewingStand

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables highlighting for brewing stands.
- **Color** (Color) — Sets the highlight color for brewing stands.
- **Tracers** (Toggle) — default: `false` — Draws tracer lines to brewing stands.

#### Dispenser

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables highlighting for dispensers.
- **Color** (Color) — Sets the highlight color for dispensers.
- **Tracers** (Toggle) — default: `false` — Draws tracer lines to dispensers.

#### Hopper

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables highlighting for hoppers.
- **Color** (Color) — Sets the highlight color for hoppers.
- **Tracers** (Toggle) — default: `false` — Draws tracer lines to hoppers.

#### ShulkerBox

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables highlighting for shulker boxes.
- **Color** (Color) — Sets the highlight color for shulker boxes.
- **Tracers** (Toggle) — default: `false` — Draws tracer lines to shulker boxes.

#### Pot

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables highlighting for decorated pots.
- **Color** (Color) — Sets the highlight color for decorated pots.
- **Tracers** (Toggle) — default: `false` — Draws tracer lines to decorated pots.

#### Shelf

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true` — Enables highlighting for shelves.
- **Color** (Color) — Sets the highlight color for shelves.
- **Tracers** (Toggle) — default: `false` — Draws tracer lines to shelves.

- **RequiresChestStealer** (Toggle) — default: `false` — Only activates StorageESP when ChestStealer module is running.
#### DistanceFade

A group of related settings.

- **NearStart** (Decimal) — default: `0.0`; range: `0.0` – `512.0` — Sets the distance where near fade-in begins.
- **NearEnd** (Decimal) — default: `0.0`; range: `0.0` – `512.0` — Sets the distance where near fade-in ends.
- **FarStart** (Decimal) — default: `512.0`; range: `0.0` – `512.0` — Sets the distance where far fade-out begins.
- **FarEnd** (Decimal) — default: `512.0`; range: `0.0` – `512.0` — Sets the distance where far fade-out ends.


### Screenshots

*Screenshots for StorageESP will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleStorageESP.kt)*
