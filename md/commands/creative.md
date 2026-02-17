## Creative Commands

Creative commands provide item manipulation features that work in Creative mode. These commands modify the item you are currently holding or give you new items.

> **Note:** Creative commands require you to be in Creative mode to function.

---

### `.give`

Give yourself an item in Creative mode.

**Usage:**
```
.give <item> [amount]
```

**Parameters:**
- `item` (required) — The item identifier (e.g. `diamond_sword`, `golden_apple`).
- `amount` (optional) — The stack size, from 1 to 64.

**Example:**
```
.give diamond_sword
.give golden_apple 64
```

---

### `.rename`

Rename the item you are currently holding.

**Usage:**
```
.rename [name]
```

**Parameters:**
- `name` (optional, vararg) — The new name for the item. Supports formatting codes. If no name is given, the item name is cleared.

**Example:**
```
.rename Super Sword
.rename
```

---

### `.enchant`

Add, remove, or manage enchantments on the item you are holding.

**Subcommands:**
- `.enchant add <enchantment> <level>` — Add an enchantment. Use `max` for the maximum level or specify a number.
- `.enchant remove <enchantment>` — Remove a specific enchantment.
- `.enchant clear` — Remove all enchantments.
- `.enchant all <level>` — Add all enchantments at the specified level.
- `.enchant all_possible <level>` — Add all compatible enchantments at the specified level.

**Parameters:**
- `enchantment` — The enchantment name (e.g. `sharpness`, `protection`).
- `level` — The enchantment level (number or `max`).

**Example:**
```
.enchant add sharpness max
.enchant add protection 4
.enchant remove sharpness
.enchant clear
.enchant all max
.enchant all_possible max
```

---

### `.skull`

Give yourself a player head (skull) with a specific player's skin.

**Usage:**
```
.skull <player>
```

**Parameters:**
- `player` (required) — The username of the player whose head you want.

**Example:**
```
.skull Notch
```

---

### `.stack`

Set the stack size of the item you are currently holding.

**Usage:**
```
.stack [amount]
```

**Parameters:**
- `amount` (optional) — The new stack size, from 1 to 64.

**Example:**
```
.stack 64
```
