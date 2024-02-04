## ItemUtil

The ItemUtil class provides methods for the creation of items.

### Method summary

#### `ItemUtil.create(arguments: string): ItemStack`
Returns an `ItemStack` with one item of the given `arguments`. <br>
List of parameters:
- `arguments`, the arguments to create the item with (same syntax to /give command).

#### `ItemUtil.create(arguments: string, amount: int): ItemStack`
Returns an `ItemStack` with `amount` items of the given `arguments`. <br>
List of parameters:
- `arguments`, the arguments to create the item with (same syntax to /give command).
- `amount`, the amount of items in the item stack.

**Example:**

```js
ItemUtil.create('minecraft:player_head{SkullOwner:"notch"}');
```