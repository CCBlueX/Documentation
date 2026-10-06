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

**Parameters:**
- `page` (optional) — The page to show, the first one by default. The arrows at the end of the list move between pages.

Every item is listed by its `author/name`, which you can click to fill in a subscribe or unsubscribe command for it.

---

#### `.marketplace search`

Search for items on the marketplace. The results are listed the same way as `.marketplace list`.

**Usage:**
```
.marketplace search <query> [page]
```

**Parameters:**
- `query` (required) — The search term.
- `page` (optional) — The page of results to show, the first one by default.

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

Subscribing also installs the add-ons and scripts the item needs, including whatever those need themselves, and LiquidBounce names the ones it installed alongside it. Restart the game to finish installing add-ons. If something the item needs does not fit the game you are running, the item is left out as well and LiquidBounce names what is missing.

---

#### `.marketplace unsubscribe`

Unsubscribe from a marketplace item.

**Usage:**
```
.marketplace unsubscribe <item>
```

**Parameters:**
- `item` (required) — The subscribed item, given as its ID, its name or `author/name`. Tab completion suggests the items you are subscribed to. If the name you give belongs to several of your subscriptions, nothing is unsubscribed and the client lists their `author/name` for you to pick from.

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
