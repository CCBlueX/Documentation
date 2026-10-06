## In-Game Commands

In-game commands allow gathering information about your account, server, and position, as well as use a few one-time-use modules.

---

### `.ping`

Display your current network latency (ping) to the server in milliseconds.

**Usage:**
```
.ping
```

---

### `.tps`

Display the current server ticks-per-second (TPS). A healthy server runs at 20 TPS.

**Usage:**
```
.tps
```

---

### `.center`

Teleports your player to the center of the current block position.

**Usage:**
```
.center
```

---

### `.coordinates`

Display, copy, or share your current coordinates.

**Aliases:** `position`, `coords`

**Subcommands:**
- `.coordinates info` — Display your current X, Y, Z coordinates.
- `.coordinates copy` — Copy your coordinates to the clipboard.
- `.coordinates whisper <player>` — Send your coordinates as a private message to another player.

**Example:**
```
.coordinates info
.coordinates copy
.coordinates whisper Steve
```

---

### `.username`

Display your current Minecraft username and copy it to the clipboard.

**Usage:**
```
.username
```

---

### `.say`

Send a chat message to the server, bypassing the client command system.

**Usage:**
```
.say <message>
```

**Parameters:**
- `message` (required, vararg) — The message to send.

**Example:**
```
.say Hello everyone!
```

> **Tip:** Useful for sending messages that start with the command prefix (e.g. `.say .help` sends ".help" as a chat message).

---

### `.serverinfo`

Display detailed information about the current server, including address, Minecraft version, TPS, and optionally detect plugins or hosting provider.

**Usage:**
```
.serverinfo [detect]
```

**Parameters:**
- `detect` (optional) — Detection type: `Plugins` or `Hosting`.
  - `Plugins` — Attempts to detect server plugins and anti-cheat software.
  - `Hosting` — Attempts to identify the server hosting provider.

**Example:**
```
.serverinfo
.serverinfo Plugins
.serverinfo Hosting
```

---

### `.remoteview`

Change your camera perspective to view from another player's position.

**Aliases:** `rv`

**Subcommands:**
- `.remoteview view <player>` — View from another player's perspective.
- `.remoteview off` — Return to your own perspective.

**Example:**
```
.remoteview view Steve
.rv off
```

---

### `.fakeplayer`

Spawn client-side fake players for testing combat modules and practicing.

**Subcommands:**
- `.fakeplayer spawn [name]` — Spawn a fake player with an optional name.
- `.fakeplayer remove [name]` — Remove a specific fake player.
- `.fakeplayer clear` — Remove all fake players.
- `.fakeplayer startrecording` — Start recording your movements for playback.
- `.fakeplayer endrecording` — Stop recording and create a moving fake player.

**Example:**
```
.fakeplayer spawn TestDummy
.fakeplayer startrecording
.fakeplayer endrecording
.fakeplayer clear
```

> **Note:** Fake players are only visible to you (client-side). They are useful for testing KillAura, Aimbot, and other combat features.
