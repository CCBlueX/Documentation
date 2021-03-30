## Chat
The Chat class simplifies interacting with the Minecraft Chat.

### Method Summary
#### Chat.print(text)
Prints the passed string client-side in the chat. <br>
List of arguments:
- text, the string to be printed to the chat.

Example:
```js
Chat.print("Axolotl are epic!")
```

## Setting
The Setting class allows the creation of module settings. With them, the behavior of a module can be adjusted by the user.

### Method Summary
#### Setting.boolean(options)
Creates a new instance of [BoolValue](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/value/Value.kt) and returns it. It can be either on or off. <br>
The following table describes the properties of the `options` object.

| Property | Description                                | Type    |
|----------|--------------------------------------------|---------|
| name     | Name under which the setting is displayed. | string  |
| default  | Default value.                             | boolean |
Example:
```js
Setting.boolean({
    name: "myBooleanSetting",
    default: true
});
```
---
#### Setting.integer(options)
Creates a new instance of [IntegerValue](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/value/Value.kt) and returns it. Allows the user to select an integer value from a range between the min and max value. <br>
The following table describes the properties of the `options` object.

| Property | Description                                | Type   |
|----------|--------------------------------------------|--------|
| name     | Name under which the setting is displayed. | string |
| default  | Default value.                             | number |
| min      | Smallest possible value.                   | number |
| max      | Largest possible value.                    | number |
Example:
```js
Setting.integer({
    name: "myIntegerSetting",
    default: 2,
    min: 1,
    max: 5
});
```
---
#### Setting.float(options)
Creates a new instance of [FloatValue](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/value/Value.kt) and returns it. Allows the user to select a floating-point value from a range between the min and max value. <br>
The following table describes the properties of the `options` object.

| Property | Description                                | Type   |
|----------|--------------------------------------------|--------|
| name     | Name under which the setting is displayed. | string |
| default  | Default value.                             | number |
| min      | Smallest possible value.                   | number |
| max      | Largest possible value.                    | number |
Example:
```js
Setting.float({
    name: "myFloatSetting",
    default: 3.5,
    min: 1.0,
    max: 5.0
});
```
---
#### Setting.text(object)
Creates a new instance of [TextValue](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/value/Value.kt) and returns it. Allows the user to specify a string as the value of this setting. <br>
The following table describes the properties of the `options` object.

| Property | Description                                | Type   |
|----------|--------------------------------------------|--------|
| name     | Name under which the setting is displayed. | string |
| default  | Default value.                             | string |
Example:
```js
Setting.text({
    name: "myTextSetting",
    default: "This is the default value."
});
```
---
#### Setting.block(options)
Creates a new instance of [BlockValue](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/value/Value.kt) and returns it. Allows the user to specify a Minecraft block as the value of this setting. <br>
The following table describes the properties of the `options` object.

| Property | Description                                | Type   |
|----------|--------------------------------------------|--------|
| name     | Name under which the setting is displayed. | string |
| default  | Default block ID.                          | number |
Example:
```js
Setting.block({
    name: "myBlockSetting",
    default: 12
});
```
---
#### Setting.list(options)
Creates a new instance of [ListValue](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/value/Value.kt) and returns it. Allows the user to select a single value from a list of available values. <br>
The following table describes the properties of the `options` object.

| Property | Description                                | Type   |
|----------|--------------------------------------------|--------|
| name     | Name under which the setting is displayed. | string |
| default  | Default value.                             | string |
| values   | Array containing all possible values.      | array  |
Example:
```js
Setting.list({
    name: "myListSetting",
    default: "Axolotl",
    values: ["Blobfish", "Axolotl", "Stork"]
});
```

## Item
The Item class allows the simple creation of an ItemStack using all necessary information about the desired block.
### Method Summary
#### Item.create(itemData)
Returns an ItemStack that matches the specified NBT data.
List of arguments:
- itemData, string containing all necessary information about the desired block.

Example:
```js
Item.create("name_tag 1 0 {display:{Name: \"Hello!\"}}");
```
