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
.marketplace subscribe <item>
```

**Parameters:**
- `item` (required) — The marketplace item, given as its ID, its name or `author/name`. Names containing spaces have to be quoted, for example `.marketplace subscribe "Author/Item Name"`. Tab completion suggests the items you are not subscribed to yet as `author/name`.

---

#### `.marketplace unsubscribe`

Unsubscribe from a marketplace item.

**Usage:**
```
.marketplace unsubscribe <item>
```

**Parameters:**
- `item` (required) — The subscribed item, given as its ID, its name or `author/name`. Tab completion suggests the items you are subscribed to. If the name you give belongs to several of your subscriptions, nothing is unsubscribed and the client lists what tells them apart.

---

#### `.marketplace update`

Update all subscribed marketplace items to their latest versions, or only the one you name.

**Usage:**
```
.marketplace update [item]
```

**Parameters:**
- `item` (optional) — The subscribed item to update, given as its ID, its name or `author/name`, the same way as for `.marketplace unsubscribe`. Without it, every subscription is updated.

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
