## AntiBot

Detects bots spawned by Anti-Cheats and prevents you from attacking them.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Custom | modes: Custom, Matrix, IntaveHeavy, Horizon)
│   ├── [Mode: Custom]
│   │   ├── Conditions (Multi-Select | default: [NoGameMode, IllegalPitch, FakeEntityID] | options: Duplicate, NoGameMode, IllegalPitch, FakeEntityID, NeedHit, IllegalHealth, Swung, Critted, Attributes, IllegalScale)
│   │   ├── InvalidGround (Toggleable Group | default: on)
│   │   │   ├── Enabled (Toggle | default: true)
│   │   │   └── VLToConsiderAsBot (Integer | default: 10 | range: 1..50 | flags)
│   │   ├── AlwaysInRadius (Toggleable Group | default: off)
│   │   │   ├── Enabled (Toggle | default: false)
│   │   │   └── AlwaysInRadiusRange (Decimal | default: 20.0 | range: 5.0..30.0)
│   │   ├── Age (Toggleable Group | default: off)
│   │   │   ├── Enabled (Toggle | default: false)
│   │   │   └── Minimum (Integer | default: 20 | range: 0..120 | ticks)
│   │   ├── Armor (Toggleable Group | default: off)
│   │   │   ├── Enabled (Toggle | default: false)
│   │   │   ├── Helmet (Multi-Select | default: [Nothing] | options: Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite, TurtleScute, Pumpkin, Skull)
│   │   │   ├── Chestplate (Multi-Select | default: [Nothing] | options: Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite, Elytra)
│   │   │   ├── Leggings (Multi-Select | default: [Nothing] | options: Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite)
│   │   │   └── Boots (Multi-Select | default: [Nothing] | options: Nothing, Leather, Chain, Iron, Gold, Diamond, Netherite)
│   │   └── Name (Toggleable Group | default: on)
│   │       ├── Enabled (Toggle | default: true)
│   │       ├── Length (Integer Range | default: 3..16 | range: 1..32)
│   │       └── ValidateChars (Multi-Select | default: [Vanilla] | options: Vanilla, Cyrillic, CJKUnifiedIdeographs)
└── LiteralNPC (Toggle | default: false)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Custom**, **Matrix**, **IntaveHeavy**, **Horizon**. Default: **Custom**.

##### Mode: Custom

- **Conditions** (Multi-Select) — default: `NoGameMode`, `IllegalPitch`, `FakeEntityID`; options: `Duplicate`, `NoGameMode`, `IllegalPitch`, `FakeEntityID`, `NeedHit`, `IllegalHealth`, `Swung`, `Critted`, `Attributes`, `IllegalScale`
###### InvalidGround

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **VLToConsiderAsBot** (Integer) — default: `10`; range: `1` – `50`; unit: flags

###### AlwaysInRadius

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **AlwaysInRadiusRange** (Decimal) — default: `20.0`; range: `5.0` – `30.0`

###### Age

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Minimum** (Integer) — default: `20`; range: `0` – `120`; unit: ticks

###### Armor

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Helmet** (Multi-Select) — default: `Nothing`; options: `Nothing`, `Leather`, `Chain`, `Iron`, `Gold`, `Diamond`, `Netherite`, `TurtleScute`, `Pumpkin`, `Skull`
- **Chestplate** (Multi-Select) — default: `Nothing`; options: `Nothing`, `Leather`, `Chain`, `Iron`, `Gold`, `Diamond`, `Netherite`, `Elytra`
- **Leggings** (Multi-Select) — default: `Nothing`; options: `Nothing`, `Leather`, `Chain`, `Iron`, `Gold`, `Diamond`, `Netherite`
- **Boots** (Multi-Select) — default: `Nothing`; options: `Nothing`, `Leather`, `Chain`, `Iron`, `Gold`, `Diamond`, `Netherite`

###### Name

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Length** (Integer Range) — default: `3` – `16`; range: `1` – `32`
- **ValidateChars** (Multi-Select) — default: `Vanilla`; options: `Vanilla`, `Cyrillic`, `CJKUnifiedIdeographs`


- **LiteralNPC** (Toggle) — default: `false`

### Screenshots

*Screenshots for AntiBot will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleAntiBot.kt)*
