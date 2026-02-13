## AutoQueue

Automatically enters mini game queues on servers.

**Category:** Player  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
└── Presets (Mode Selector | default: HypixelSW | modes: HypixelSW, GommeDuels, Custom)
    ├── [Mode: HypixelSW]
    │   └── GameMode (Choice | default: NORMAL | options: Normal, Insane)
    ├── [Mode: GommeDuels]
    │   ├── WinMessage (Text)
    │   ├── LoseMessage (Text)
    │   └── ControlKillAura (Toggle | default: true)
    └── [Mode: Custom]
        ├── Trigger (Mode Selector | default: Title | modes: Title, Title, Message, Item, TabHeader, TabFooter)
        │   ├── [Mode: Title]
        │   │   └── Keywords (Editable List)
        │   ├── [Mode: Title]
        │   │   └── Keywords (Editable List)
        │   ├── [Mode: Message]
        │   │   ├── Keywords (Editable List)
        │   │   └── ChatTypes (Multi-Select | default: [GameMessage] | options: ChatMessage, DisguisedChatMessage, GameMessage)
        │   ├── [Mode: Item]
        │   │   └── Mode (Mode Selector | default: Name | modes: Name, Item)
        │   │       ├── [Mode: Name]
        │   │       │   ├── Names (Editable List)
        │   │       │   └── Mode (Choice | default: EQUALS | options: Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase)
        │   │       └── [Mode: Item]
        │   │           └── Items (Registry List)
        │   ├── [Mode: TabHeader]
        │   │   └── Text (Text)
        │   └── [Mode: TabFooter]
        │       └── Text (Text)
        ├── Action (Mode Selector | default: Chat | modes: Chat, UseItem)
        │   ├── [Mode: Chat]
        │   │   ├── StartDelay (Integer Range | default: 0..0 | range: 0..5000 | ms)
        │   │   ├── MessageDelay (Integer Range | default: 0..0 | range: 0..5000 | ms)
        │   │   └── Messages (Editable List)
        │   └── [Mode: UseItem]
        │       └── Mode (Mode Selector | default: Name | modes: Name, Item)
        │           ├── [Mode: Name]
        │           │   ├── Names (Editable List)
        │           │   └── Mode (Choice | default: EQUALS | options: Equals, EqualsIgnoreCase, Contains, ContainsIgnoreCase, StartsWith, StartsWithIgnoreCase, EndsWith, EndsWithIgnoreCase)
        │           └── [Mode: Item]
        │               └── Items (Registry List)
        ├── Control (Toggleable Group | default: on)
        │   ├── Enabled (Toggle | default: true)
        │   ├── KillAura (Toggle | default: true)
        │   └── Speed (Toggle | default: false)
        └── WaitUntilWorldChange (Toggle | default: true)
```

### Settings Details

#### Presets

Select a mode for this feature. Available modes: **HypixelSW**, **GommeDuels**, **Custom**. Default: **HypixelSW**.

##### Mode: HypixelSW

- **GameMode** (Choice) — default: `NORMAL`; options: `Normal`, `Insane`

##### Mode: GommeDuels

- **WinMessage** (Text)
- **LoseMessage** (Text)
- **ControlKillAura** (Toggle) — default: `true`

##### Mode: Custom

###### Trigger

Select a mode for this feature. Available modes: **Title**, **Title**, **Message**, **Item**, **TabHeader**, **TabFooter**. Default: **Title**.

###### Mode: Title

- **Keywords** (Editable List)

###### Mode: Title

- **Keywords** (Editable List)

###### Mode: Message

- **Keywords** (Editable List)
- **ChatTypes** (Multi-Select) — default: `GameMessage`; options: `ChatMessage`, `DisguisedChatMessage`, `GameMessage`

###### Mode: Item

###### Mode

Select a mode for this feature. Available modes: **Name**, **Item**. Default: **Name**.

###### Mode: Name

- **Names** (Editable List)
- **Mode** (Choice) — default: `EQUALS`; options: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, `EndsWithIgnoreCase`

###### Mode: Item

- **Items** (Registry List)


###### Mode: TabHeader

- **Text** (Text)

###### Mode: TabFooter

- **Text** (Text)

###### Action

Select a mode for this feature. Available modes: **Chat**, **UseItem**. Default: **Chat**.

###### Mode: Chat

- **StartDelay** (Integer Range) — default: `0` – `0`; range: `0` – `5000`; unit: ms
- **MessageDelay** (Integer Range) — default: `0` – `0`; range: `0` – `5000`; unit: ms
- **Messages** (Editable List)

###### Mode: UseItem

###### Mode

Select a mode for this feature. Available modes: **Name**, **Item**. Default: **Name**.

###### Mode: Name

- **Names** (Editable List)
- **Mode** (Choice) — default: `EQUALS`; options: `Equals`, `EqualsIgnoreCase`, `Contains`, `ContainsIgnoreCase`, `StartsWith`, `StartsWithIgnoreCase`, `EndsWith`, `EndsWithIgnoreCase`

###### Mode: Item

- **Items** (Registry List)


###### Control

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **KillAura** (Toggle) — default: `true`
- **Speed** (Toggle) — default: `false`

- **WaitUntilWorldChange** (Toggle) — default: `true`


### Screenshots

*Screenshots for AutoQueue will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fplayer%2FModuleAutoQueue.kt)*
