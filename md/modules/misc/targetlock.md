## TargetLock

Makes you attack only one specific enemy.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Mode (Mode Selector | default: Temporary | modes: Temporary, Filter)
│   ├── [Mode: Temporary]
│   │   ├── MaximumTime (Integer | default: 30 | range: 0..120 | s)
│   │   ├── MaximumRange (Decimal | default: 20.0 | range: 8.0..40.0)
│   │   └── WhenNoLock (Choice | default: ALLOW_ALL | options: AllowAll, AllowNone)
│   └── [Mode: Filter]
│       ├── Usernames (Editable List)
│       └── FilterType (Choice | default: WHITELIST | options: Whitelist, Blacklist)
└── Combat (Toggle | default: false)
```

### Settings Details

#### Mode

Select a mode for this feature. Available modes: **Temporary**, **Filter**. Default: **Temporary**.

##### Mode: Temporary

- **MaximumTime** (Integer) — default: `30`; range: `0` – `120`; unit: s
- **MaximumRange** (Decimal) — default: `20.0`; range: `8.0` – `40.0`
- **WhenNoLock** (Choice) — default: `ALLOW_ALL`; options: `AllowAll`, `AllowNone`

##### Mode: Filter

- **Usernames** (Editable List)
- **FilterType** (Choice) — default: `WHITELIST`; options: `Whitelist`, `Blacklist`

- **Combat** (Toggle) — default: `false`

### Screenshots

*Screenshots for TargetLock will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleTargetLock.kt)*
