## ItemUtil

The ItemUtil class provides methods for the creation of items.

### Method summary

#### `ItemUtil.create(arguments: string): ItemStack`
Returns an *ItemStack* with one item of the given *arguments*. <br>
List of parameters:
- *arguments*, the arguments to create the item with (same syntax as the /give command).

<hr>

#### `ItemUtil.create(arguments: string, amount: int): ItemStack`
Returns an *ItemStack* with *amount* items of the given *arguments*. <br>
List of parameters:
- *arguments*, the arguments to create the item with (same syntax as the /give command).
- *amount*, the amount of items in the item stack.

**Example:**

```js
ItemUtil.create('minecraft:player_head[profile={name:"Notch"}]');
```

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptItemUtil.kt)*
