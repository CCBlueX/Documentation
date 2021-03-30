## ScriptAPI inventory tabs
LiquidBounce has a secondary inventory that can be accessed in creative mode. It contains useful items, but also items that can be used to exploit in-game bugs. With the ScriptAPI it is also possible to add additional tabs with your own items.

### Creating a tab
#### script.registerTab(options)
The registerTab method allows the addition of a separate tab to the secondary inventory, which can contain special items, including items with unique NBT data. It creates a new instance of [ScriptTab](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/script/api/ScriptTab.kt) and registers it with the client. <br>
The following table describes the properties of the `options` object.

| Property | Description                                                                      | Type   |
|----------|----------------------------------------------------------------------------------|--------|
| name     | Name under which the tab will be shown in the inventory.                         | string |
| icon     | Icon the tab will have in the inventory. Has to be the name of an existing item. | string |
| items    | Array containing the items of the tab.                                           | array  |
Example:
```js
script.registerTab({
    name: "MyTab",
    icon: "apple",
    items: [
        Item.create("dirt")
    ]
});
```

Hint: The global Item class of the ScriptAPI proves to be very useful here to create items with special NBT data. Its documentation can be found [here](/docs/ScriptAPI/Global%20Classes).