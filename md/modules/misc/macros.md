## Macros

Lets you execute chat messages or item actions using custom keybinds.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Chat-1 (Setting Group)
│   ├── TriggerDelay (Integer Range | default: 0..0 | range: 0..15000 | ms)
│   ├── Trigger (Key)
│   ├── Delay (Integer Range | default: 0..0 | range: 0..5000 | ms)
│   └── Messages (Editable List)
├── Chat-2 (Setting Group)
│   ├── TriggerDelay (Integer Range | default: 0..0 | range: 0..15000 | ms)
│   ├── Trigger (Key)
│   ├── Delay (Integer Range | default: 0..0 | range: 0..5000 | ms)
│   └── Messages (Editable List)
├── Chat-3 (Setting Group)
│   ├── TriggerDelay (Integer Range | default: 0..0 | range: 0..15000 | ms)
│   ├── Trigger (Key)
│   ├── Delay (Integer Range | default: 0..0 | range: 0..5000 | ms)
│   └── Messages (Editable List)
├── Chat-4 (Setting Group)
│   ├── TriggerDelay (Integer Range | default: 0..0 | range: 0..15000 | ms)
│   ├── Trigger (Key)
│   ├── Delay (Integer Range | default: 0..0 | range: 0..5000 | ms)
│   └── Messages (Editable List)
├── Chat-5 (Setting Group)
│   ├── TriggerDelay (Integer Range | default: 0..0 | range: 0..15000 | ms)
│   ├── Trigger (Key)
│   ├── Delay (Integer Range | default: 0..0 | range: 0..5000 | ms)
│   └── Messages (Editable List)
├── Item-1 (Setting Group)
│   ├── TriggerDelay (Integer Range | default: 0..0 | range: 0..15000 | ms)
│   ├── Trigger (Key)
│   ├── Action (Choice | default: USE_ONLY | options: UseOnly, PlaceOrUse)
│   ├── PickMode (Mode Selector | default: Name | modes: Name, Item)
│   │   ├── [Mode: Name]
│   │   │   ├── Names (Editable List)
│   │   │   └── Mode (Choice | default: EQUALS | options: Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase)
│   │   └── [Mode: Item]
│   │       └── Items (Registry List)
│   ├── SwingMode (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│   └── HoldTime (Integer Range | default: 1..1 | range: 1..20 | ticks)
├── Item-2 (Setting Group)
│   ├── TriggerDelay (Integer Range | default: 0..0 | range: 0..15000 | ms)
│   ├── Trigger (Key)
│   ├── Action (Choice | default: USE_ONLY | options: UseOnly, PlaceOrUse)
│   ├── PickMode (Mode Selector | default: Name | modes: Name, Item)
│   │   ├── [Mode: Name]
│   │   │   ├── Names (Editable List)
│   │   │   └── Mode (Choice | default: EQUALS | options: Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase)
│   │   └── [Mode: Item]
│   │       └── Items (Registry List)
│   ├── SwingMode (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│   └── HoldTime (Integer Range | default: 1..1 | range: 1..20 | ticks)
├── Item-3 (Setting Group)
│   ├── TriggerDelay (Integer Range | default: 0..0 | range: 0..15000 | ms)
│   ├── Trigger (Key)
│   ├── Action (Choice | default: USE_ONLY | options: UseOnly, PlaceOrUse)
│   ├── PickMode (Mode Selector | default: Name | modes: Name, Item)
│   │   ├── [Mode: Name]
│   │   │   ├── Names (Editable List)
│   │   │   └── Mode (Choice | default: EQUALS | options: Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase)
│   │   └── [Mode: Item]
│   │       └── Items (Registry List)
│   ├── SwingMode (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│   └── HoldTime (Integer Range | default: 1..1 | range: 1..20 | ticks)
├── Item-4 (Setting Group)
│   ├── TriggerDelay (Integer Range | default: 0..0 | range: 0..15000 | ms)
│   ├── Trigger (Key)
│   ├── Action (Choice | default: USE_ONLY | options: UseOnly, PlaceOrUse)
│   ├── PickMode (Mode Selector | default: Name | modes: Name, Item)
│   │   ├── [Mode: Name]
│   │   │   ├── Names (Editable List)
│   │   │   └── Mode (Choice | default: EQUALS | options: Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase)
│   │   └── [Mode: Item]
│   │       └── Items (Registry List)
│   ├── SwingMode (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
│   └── HoldTime (Integer Range | default: 1..1 | range: 1..20 | ticks)
└── Item-5 (Setting Group)
    ├── TriggerDelay (Integer Range | default: 0..0 | range: 0..15000 | ms)
    ├── Trigger (Key)
    ├── Action (Choice | default: USE_ONLY | options: UseOnly, PlaceOrUse)
    ├── PickMode (Mode Selector | default: Name | modes: Name, Item)
    │   ├── [Mode: Name]
    │   │   ├── Names (Editable List)
    │   │   └── Mode (Choice | default: EQUALS | options: Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase)
    │   └── [Mode: Item]
    │       └── Items (Registry List)
    ├── SwingMode (Choice | default: DO_NOT_HIDE | options: DoNotHide, HideForBoth, HideForClient, HideForServer)
    └── HoldTime (Integer Range | default: 1..1 | range: 1..20 | ticks)
```

### Settings Details

#### Chat-1

A group of related settings.

- **TriggerDelay** (Integer Range) — default: `0` – `0`; range: `0` – `15000`; unit: ms
- **Trigger** (Key)
- **Delay** (Integer Range) — default: `0` – `0`; range: `0` – `5000`; unit: ms
- **Messages** (Editable List)

#### Chat-2

A group of related settings.

- **TriggerDelay** (Integer Range) — default: `0` – `0`; range: `0` – `15000`; unit: ms
- **Trigger** (Key)
- **Delay** (Integer Range) — default: `0` – `0`; range: `0` – `5000`; unit: ms
- **Messages** (Editable List)

#### Chat-3

A group of related settings.

- **TriggerDelay** (Integer Range) — default: `0` – `0`; range: `0` – `15000`; unit: ms
- **Trigger** (Key)
- **Delay** (Integer Range) — default: `0` – `0`; range: `0` – `5000`; unit: ms
- **Messages** (Editable List)

#### Chat-4

A group of related settings.

- **TriggerDelay** (Integer Range) — default: `0` – `0`; range: `0` – `15000`; unit: ms
- **Trigger** (Key)
- **Delay** (Integer Range) — default: `0` – `0`; range: `0` – `5000`; unit: ms
- **Messages** (Editable List)

#### Chat-5

A group of related settings.

- **TriggerDelay** (Integer Range) — default: `0` – `0`; range: `0` – `15000`; unit: ms
- **Trigger** (Key)
- **Delay** (Integer Range) — default: `0` – `0`; range: `0` – `5000`; unit: ms
- **Messages** (Editable List)

#### Item-1

A group of related settings.

- **TriggerDelay** (Integer Range) — default: `0` – `0`; range: `0` – `15000`; unit: ms
- **Trigger** (Key)
- **Action** (Choice) — default: `USE_ONLY`; options: `UseOnly`, `PlaceOrUse`
##### PickMode

Select a mode for this feature. Available modes: **Name**, **Item**. Default: **Name**.

###### Mode: Name

- **Names** (Editable List)
- **Mode** (Choice) — default: `EQUALS`; options: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, `EndsWithIgnoreCase`

###### Mode: Item

- **Items** (Registry List)

- **SwingMode** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **HoldTime** (Integer Range) — default: `1` – `1`; range: `1` – `20`; unit: ticks

#### Item-2

A group of related settings.

- **TriggerDelay** (Integer Range) — default: `0` – `0`; range: `0` – `15000`; unit: ms
- **Trigger** (Key)
- **Action** (Choice) — default: `USE_ONLY`; options: `UseOnly`, `PlaceOrUse`
##### PickMode

Select a mode for this feature. Available modes: **Name**, **Item**. Default: **Name**.

###### Mode: Name

- **Names** (Editable List)
- **Mode** (Choice) — default: `EQUALS`; options: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, `EndsWithIgnoreCase`

###### Mode: Item

- **Items** (Registry List)

- **SwingMode** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **HoldTime** (Integer Range) — default: `1` – `1`; range: `1` – `20`; unit: ticks

#### Item-3

A group of related settings.

- **TriggerDelay** (Integer Range) — default: `0` – `0`; range: `0` – `15000`; unit: ms
- **Trigger** (Key)
- **Action** (Choice) — default: `USE_ONLY`; options: `UseOnly`, `PlaceOrUse`
##### PickMode

Select a mode for this feature. Available modes: **Name**, **Item**. Default: **Name**.

###### Mode: Name

- **Names** (Editable List)
- **Mode** (Choice) — default: `EQUALS`; options: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, `EndsWithIgnoreCase`

###### Mode: Item

- **Items** (Registry List)

- **SwingMode** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **HoldTime** (Integer Range) — default: `1` – `1`; range: `1` – `20`; unit: ticks

#### Item-4

A group of related settings.

- **TriggerDelay** (Integer Range) — default: `0` – `0`; range: `0` – `15000`; unit: ms
- **Trigger** (Key)
- **Action** (Choice) — default: `USE_ONLY`; options: `UseOnly`, `PlaceOrUse`
##### PickMode

Select a mode for this feature. Available modes: **Name**, **Item**. Default: **Name**.

###### Mode: Name

- **Names** (Editable List)
- **Mode** (Choice) — default: `EQUALS`; options: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, `EndsWithIgnoreCase`

###### Mode: Item

- **Items** (Registry List)

- **SwingMode** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **HoldTime** (Integer Range) — default: `1` – `1`; range: `1` – `20`; unit: ticks

#### Item-5

A group of related settings.

- **TriggerDelay** (Integer Range) — default: `0` – `0`; range: `0` – `15000`; unit: ms
- **Trigger** (Key)
- **Action** (Choice) — default: `USE_ONLY`; options: `UseOnly`, `PlaceOrUse`
##### PickMode

Select a mode for this feature. Available modes: **Name**, **Item**. Default: **Name**.

###### Mode: Name

- **Names** (Editable List)
- **Mode** (Choice) — default: `EQUALS`; options: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, `EndsWithIgnoreCase`

###### Mode: Item

- **Items** (Registry List)

- **SwingMode** (Choice) — default: `DO_NOT_HIDE`; options: `DoNotHide`, `HideForBoth`, `HideForClient`, `HideForServer`
- **HoldTime** (Integer Range) — default: `1` – `1`; range: `1` – `20`; unit: ticks


### Screenshots

*Screenshots for Macros will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModuleMacros.kt)*
