## Module Commands

Module commands are tied to specific modules and provide additional functionality beyond what the module settings offer.

---

### `.xray`

Manage the list of blocks visible through XRay.

**Subcommands:**
- `.xray add <block>` — Add a block to the XRay list.
- `.xray remove <block>` — Remove a block from the XRay list.
- `.xray list` — List all blocks in the XRay filter.
- `.xray clear` — Remove all blocks from the XRay list.
- `.xray reset` — Reset the XRay list to default blocks.

**Parameters:**
- `block` — The block identifier (e.g. `diamond_ore`, `iron_ore`).

**Example:**
```
.xray add diamond_ore
.xray add ancient_debris
.xray remove iron_ore
.xray list
.xray reset
```

> **Related module:** [XRay](/docs/Modules/Render/XRay)

---

### `.autodisable`

Manage the list of modules that automatically disable on certain events (e.g. death, world change).

**Subcommands:**
- `.autodisable add <module>` — Add a module to the auto-disable list.
- `.autodisable remove <module>` — Remove a module from the auto-disable list.
- `.autodisable list` — List all auto-disable modules.
- `.autodisable clear` — Clear the auto-disable list.

**Example:**
```
.autodisable add KillAura
.autodisable add Speed
.autodisable list
```

> **Related module:** [AutoDisable](/docs/Modules/World/AutoDisable)

---

### `.autoaccount`

Manage automatic account registration and login for cracked servers.

**Subcommands:**
- `.autoaccount register` — Register an account on the current server.
- `.autoaccount login` — Log in to the current server.

> **Related module:** [AutoAccount](/docs/Modules/Misc/AutoAccount)

---

### `.invsee`

View another player's inventory (client-side reconstruction).

**Usage:**
```
.invsee <player>
```

**Parameters:**
- `player` (required) — The username of the player whose inventory you want to view.

**Example:**
```
.invsee Steve
```

> **Related module:** [InventoryTracker](/docs/Modules/World/InventoryTracker)

---

### `.teleport`

Teleport to specific coordinates using the Teleport module's exploit.

**Aliases:** `tp`

**Usage:**
```
.teleport <x> <y> <z>
```

**Parameters:**
- `x` (required) — X coordinate.
- `y` (required) — Y coordinate (or Z if only two values given).
- `z` (required) — Z coordinate.

**Example:**
```
.teleport 100 64 200
.tp 0 100 0
```

> **Related module:** [Teleport](/docs/Modules/Exploit/Teleport)

---

### `.playerteleport`

Teleport to another player's position using the Teleport module's exploit.

**Aliases:** `playertp`, `ptp`

**Usage:**
```
.playerteleport <player> [copy]
```

**Parameters:**
- `player` (required) — The username of the target player.
- `copy` (optional) — Additional option for coordinate copying.

**Example:**
```
.playerteleport Steve
.ptp Steve
```

> **Related module:** [Teleport](/docs/Modules/Exploit/Teleport)

---

### `.vclip`

Vertically clip through blocks using the Teleport module's exploit.

**Subcommands:**
- `.vclip by <distance>` — Clip vertically by a specific distance (positive = up, negative = down).
- `.vclip smart up [max]` — Intelligently clip upward through blocks. Optionally specify max distance.
- `.vclip smart down [max]` — Intelligently clip downward through blocks. Optionally specify max distance.

**Example:**
```
.vclip by 5
.vclip by -10
.vclip smart up
.vclip smart down 20
```

> **Related module:** [Teleport](/docs/Modules/Exploit/Teleport)

---

### `.models`

Manage deep learning AI models for combat prediction.

**Subcommands:**
- `.models create <name>` — Create a new AI model.
- `.models improve <name>` — Improve an existing model with new training data.
- `.models delete <name>` — Delete a model.
- `.models reload` — Reload all models.
- `.models browse` — Open the models folder.

**Example:**
```
.models create combat_v1
.models improve combat_v1
.models delete combat_v1
```
