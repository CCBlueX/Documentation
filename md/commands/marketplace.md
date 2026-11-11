## Marketplace Commands

The `.marketplace` command finds themes, add-ons and scripts on the LiquidBounce marketplace and installs them for you. To find configs, use [`.config`](/docs/commands/client) instead.

Items are named as `author/name`. You can also use just the name or the item's ID. Put names with spaces in double quotes, like `"Author/Item Name"`.

---

### `.marketplace list`

Lists the items of one kind.

```
.marketplace list <type> [page]
```

- `type`: `Theme`, `Addon` or `Script`.
- `page`: which page to show, the first one if you leave it out. Click the arrows under the list to change pages.

Click an item's name to fill in the command that installs or removes it.

```
.marketplace list Theme
.marketplace list Addon 2
```

---

### `.marketplace search`

Searches the whole marketplace. The results look like `.marketplace list` and also show what kind of item each one is.

```
.marketplace search <query> [page]
```

```
.marketplace search bedwars
.marketplace search "dark theme"
```

---

### `.marketplace subscribe`

Installs an item and keeps it updated.

```
.marketplace subscribe <item>
```

If the item needs add-ons or scripts, they are installed too, and the chat lists them. Restart the game to finish installing add-ons. If something the item needs does not work with your game version, the item is not installed and the chat tells you what is missing.

---

### `.marketplace unsubscribe`

Removes an item you installed.

```
.marketplace unsubscribe <item>
```

If the name fits more than one of your items, nothing is removed and the chat lists them as `author/name`, so you can pick the right one.

---

### `.marketplace update`

Updates your installed items to their newest versions.

```
.marketplace update [item]
```

Without an item, everything you installed is updated.

---

### `.marketplace revisions list`

Lists the versions of an item and when each one came out.

```
.marketplace revisions list <item>
```

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/command/commands/client/marketplace)*
