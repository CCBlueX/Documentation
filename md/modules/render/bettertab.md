## BetterTab

Multiple improvements to the tab list.

**Category:** Render  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Sorting (Choice | default: VANILLA | options: Vanilla, Ping, NameLength, DisplayNameLength, Alphabetical, ReverseAlphabetical, None)
├── Visibility (Multi-Select | default: [Header, Footer] | options: Header, Footer, NameOnly)
├── Limits (Setting Group)
│   ├── TabSize (Integer | default: 80 | range: 1..1000)
│   └── ColumnHeight (Integer | default: 20 | range: 1..100)
├── Highlight (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Self (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   └── Color (Color)
│   ├── Friends (Toggleable Group | default: on)
│   │   ├── Enabled (Toggle | default: true)
│   │   └── Color (Color)
│   └── Others (Toggleable Group | default: on)
│       ├── Enabled (Toggle | default: true)
│       ├── Color (Color)
│       └── Filter (Setting Group)
│           ├── FilterBy (Multi-Select | default: [DisplayName, PlayerName] | options: DisplayName, PlayerName)
│           └── Names (Editable List)
├── AccurateLatency (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   └── AppendMSSuffix (Toggle | default: true)
└── PlayerHider (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    └── Filter (Setting Group)
        ├── FilterBy (Multi-Select | default: [DisplayName, PlayerName] | options: DisplayName, PlayerName)
        └── Names (Editable List)
```

### Settings Details

- **Sorting** (Choice) — default: `VANILLA`; options: `Vanilla`, `Ping`, `NameLength`, `DisplayNameLength`, `Alphabetical`, `ReverseAlphabetical`, `None`
- **Visibility** (Multi-Select) — default: `Header`, `Footer`; options: `Header`, `Footer`, `NameOnly`
#### Limits

A group of related settings.

- **TabSize** (Integer) — default: `80`; range: `1` – `1000`
- **ColumnHeight** (Integer) — default: `20`; range: `1` – `100`

#### Highlight

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
##### Self

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Color** (Color)

##### Friends

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Color** (Color)

##### Others

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Color** (Color)
###### Filter

A group of related settings.

- **FilterBy** (Multi-Select) — default: `DisplayName`, `PlayerName`; options: `DisplayName`, `PlayerName`
- **Names** (Editable List)



#### AccurateLatency

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **AppendMSSuffix** (Toggle) — default: `true`

#### PlayerHider

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
##### Filter

A group of related settings.

- **FilterBy** (Multi-Select) — default: `DisplayName`, `PlayerName`; options: `DisplayName`, `PlayerName`
- **Names** (Editable List)



### Screenshots

*Screenshots for BetterTab will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Frender%2FModuleBetterTab.kt)*
