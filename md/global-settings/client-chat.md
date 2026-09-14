## ClientChat

Connects to **LiquidChat**, a built-in IRC-style chat system that allows LiquidBounce users to communicate with each other in real time, regardless of which Minecraft server they are on.

**Aliases:** GlobalChat, IRC  
**Toggleable:** Yes  
**Enabled by default:** Yes

### Settings

```
├── Enabled (Toggle | default: true)
├── JwtToken (Text | default: "")
├── Filter (Toggleable Group | default: false)
│   ├── Usernames (Text List | default: empty)
│   └── UsernameFilter (Choice | default: Blacklist | options: Whitelist, Blacklist)
└── AutoTranslate (Multi-Select | options: PublicChat, PrivateChat)
```

### Settings Details

- **Enabled** (Toggle) — default: `true` — Enables or disables the LiquidChat connection. When enabled, the client automatically connects to the LiquidChat server.
- **JwtToken** (Text) — default: `""` — JWT authentication token for LiquidChat. This is automatically populated when you authenticate. You can request a new token using the `.chatjwt` command.
- **Filter** (Toggleable Group) — default: `false` — When enabled, incoming LiquidChat messages are filtered by their sender's username. Filtered messages are not shown in chat; the first message hidden from a given sender is noted in the client log.
- **Filter → Usernames** (Text List) — default: empty — The usernames the filter applies to. Matching is case-insensitive.
- **Filter → UsernameFilter** (Choice) — default: `Blacklist` — How the Usernames list is interpreted. **Blacklist** hides messages from the listed senders; **Whitelist** shows messages only from the listed senders.
- **AutoTranslate** (Multi-Select) — options: `PublicChat`, `PrivateChat` — When selected, incoming messages from the chosen chat groups are automatically translated using the configured AutoTranslate provider.

### Related Commands

- `.chat <message>` — Send a message to LiquidChat.
- `.chatjwt` — Request a new JWT authentication token from the LiquidChat server.

### How It Works

1. When enabled, the client connects to the LiquidChat server automatically.
2. Authentication is handled via Mojang login or JWT token.
3. Messages appear in-game chat with a **ClientChat** prefix in blue.
4. The client automatically reconnects if the connection is lost.
5. On session change (e.g. switching Minecraft accounts), the client reconnects with the new credentials.
