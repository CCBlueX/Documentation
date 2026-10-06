## RichPresence

Displays customizable LiquidBounce information on your Discord profile through Discord Rich Presence.

**Aliases:** DiscordPresence  
**Toggleable:** Yes  
**Enabled by default:** Yes

### Settings

```
├── Enabled (Toggle | default: true)
├── ActivityType (Choice | default: Competing | options: Playing, Listening, Watching, Competing)
├── StatusDisplayType (Choice | default: Name | options: Name, State, Details)
├── Separator (Text | default: " - ")
├── DetailsParts (Multi-Select | default: [ClientName, ClientVersion, ClientAuthor] | options: ClientName, ClientVersion, ClientAuthor, Modules, Protocol, Server, Branch, Commit)
├── StateParts (Multi-Select | default: [Modules, Protocol] | options: ClientName, ClientVersion, ClientAuthor, Modules, Protocol, Server, Branch, Commit)
├── LargeImage (Toggleable Group | default: on)
│   ├── Enabled (Toggle | default: true)
│   ├── Asset (Choice | default: Logo | options: Logo)
│   └── Parts (Multi-Select | default: [Protocol] | options: ClientName, ClientVersion, ClientAuthor, Modules, Protocol, Server, Branch, Commit)
└── SmallImage (Toggleable Group | default: off)
    ├── Enabled (Toggle | default: false)
    ├── Asset (Choice | default: Logo | options: Logo)
    └── Parts (Multi-Select | default: [Branch, Commit] | options: ClientName, ClientVersion, ClientAuthor, Modules, Protocol, Server, Branch, Commit)
```

### Settings Details

- **Enabled** (Toggle) — default: `true` — Enables or disables Discord Rich Presence.
- **ActivityType** (Choice) — default: `Competing`; options: `Playing`, `Listening`, `Watching`, `Competing` — The type of activity shown on your Discord profile.
- **StatusDisplayType** (Choice) — default: `Name`; options: `Name`, `State`, `Details` — Controls how the status is displayed on Discord.
- **Separator** (Text) — default: `" - "` — The text used to separate multiple parts in the presence display.
- **DetailsParts** (Multi-Select) — default: `ClientName`, `ClientVersion`, `ClientAuthor`; options: `ClientName`, `ClientVersion`, `ClientAuthor`, `Modules`, `Protocol`, `Server`, `Branch`, `Commit` — Information shown in the Details line of the Rich Presence.
- **StateParts** (Multi-Select) — default: `Modules`, `Protocol`; options: `ClientName`, `ClientVersion`, `ClientAuthor`, `Modules`, `Protocol`, `Server`, `Branch`, `Commit` — Information shown in the State line of the Rich Presence.

#### LargeImage

A toggleable group of settings (default: enabled).

- **Enabled** (Toggle) — default: `true`
- **Asset** (Choice) — default: `Logo`; options: `Logo` — The image displayed as the large icon.
- **Parts** (Multi-Select) — default: `Protocol`; options: `ClientName`, `ClientVersion`, `ClientAuthor`, `Modules`, `Protocol`, `Server`, `Branch`, `Commit` — Tooltip text for the large image.

#### SmallImage

A toggleable group of settings (default: disabled).

- **Enabled** (Toggle) — default: `false`
- **Asset** (Choice) — default: `Logo`; options: `Logo` — The image displayed as the small icon.
- **Parts** (Multi-Select) — default: `Branch`, `Commit`; options: `ClientName`, `ClientVersion`, `ClientAuthor`, `Modules`, `Protocol`, `Server`, `Branch`, `Commit` — Tooltip text for the small image.

### Rich Presence Parts

| Part | Description |
|---|---|
| ClientName | The client name (LiquidBounce) |
| ClientVersion | The current version of the client |
| ClientAuthor | The client author (CCBlueX) |
| Modules | Active module count (e.g. "12/226 modules") |
| Protocol | The Minecraft protocol version (e.g. "1.21.4 (769)") |
| Server | The current server address (sensitive addresses are hidden) |
| Branch | The client build branch |
| Commit | The client build commit hash |

### Notes

- Discord must be running for Rich Presence to work. If Discord is not detected, a notification is shown.
- The presence updates every second (20 ticks).
- Two buttons are always shown: **Website** (liquidbounce.net) and **LiquidProxy** (liquidproxy.net).
