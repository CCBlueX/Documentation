## Marketplace Commands

Marketplace commands allow you to browse, search, subscribe to, and manage items from the LiquidBounce marketplace.

---

### `.marketplace`

The main marketplace command with multiple subcommands for interacting with the marketplace.

**Subcommands:**

#### `.marketplace list`

List available marketplace items with pagination.

**Usage:**
```
.marketplace list [page]
```

---

#### `.marketplace search`

Search for items on the marketplace.

**Usage:**
```
.marketplace search <query>
```

**Parameters:**
- `query` (required) — The search term.

**Example:**
```
.marketplace search KillAura
.marketplace search bedwars config
```

---

#### `.marketplace subscribe`

Subscribe to a marketplace item to receive its content and updates.

**Usage:**
```
.marketplace subscribe <id>
```

**Parameters:**
- `id` (required) — The marketplace item ID.

---

#### `.marketplace unsubscribe`

Unsubscribe from a marketplace item.

**Usage:**
```
.marketplace unsubscribe <id>
```

**Parameters:**
- `id` (required) — The marketplace item ID.

---

#### `.marketplace update`

Update all subscribed marketplace items to their latest versions.

**Usage:**
```
.marketplace update
```

---

#### `.marketplace revisions`

View revisions of a marketplace item.

**Usage:**
```
.marketplace revisions <id>
```

**Parameters:**
- `id` (required) — The marketplace item ID.

---
