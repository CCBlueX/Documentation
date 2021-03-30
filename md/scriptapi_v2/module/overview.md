## ScriptAPI modules
Modules created with the script API appear in both the ClickGUI and the TabGUI. They behave just like regular modules and can be customized with settings, bound to keys and enabled or disabled.

### Creating a module
#### script.registerModule(options, callback)
Each module has to be registered with the client via the instance of the script. This is done using the `registerModule` method. It creates a new instance of [ScriptModule](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/script/api/ScriptModule.kt) and passes it to the callback function. <br>
The following table describes the properties of the `options` object.

| Property    | Description                                                            | Type   |
|-------------|------------------------------------------------------------------------|--------|
| name        | Name under which the module is displayed.                              | string |
| category    | Category under which the module is displayed.                          | string |
| description | Description of what the modules does.                                  | string |
| tag         | String displayed next the to module name in the array list (optional). | string |
| settings    | Object containing all settings of the module (optional).               | object |
`options.category` can be one of the following:
- Misc
- Movement
- Exploit
- Render
- Combat
- Player
- Fun
- World

`options.tag` can be overridden by setting `module.tag` to a new value.

`options.settings` contains all settings. More information on creating a setting can be found [here](/docs/ScriptAPI/Global%20Classes).

Example:
```js
script.registerModule({
    name: "TestModule",
    category: "Misc",
    description: "This module is using LiquidBounce's ScriptAPI.",
    tag: "Test",
    settings: {
        myBooleanSetting: Setting.boolean({
            name: "MyBooleanSetting",
            default: false
        })
    }
}, function(module) {

});
```

### Handling events
Script modules also use LiquidBounce's event system. Each event used has to be registered with the client along with a handler function that will be called by the client whenever the event occurs. The [ScriptModule](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/script/api/ScriptModule.kt) class has a method for this purpose.
### module.on(eventName, callback)
Registers the use of an event with the client.
List of arguments:
- eventName, name of the event to be handled.
- callback, function called whenever the event occurs.

Example:
```js
module.on("enable", function() {
    Chat.print("The module is now enabled.");
});
```

### Getting a setting
If a setting was specified in the settings object when the module was registered, it can be accessed as follows via the key defined in the settings object.
```js
module.settings.myBooleanSetting;
```
For more information, please refer to the documentation on [settings](/docs/ScriptAPI/Creating%20Modules/Settings).

### Overwrite the module tag
It is possible to overwrite the module tag even after registration. This is especially useful if it should indicate the mode of the module. This is done as follows.
```js
module.tag = "NewTag";
```

### Full example of a module
```js
script.registerModule({
    name: "TestModule",
    category: "Misc",
    description: "This module is using LiquidBounce's ScriptAPI.",
    tag: "Test",
    settings: {
        myBooleanSetting: Setting.boolean({
            name: "MyBooleanSetting",
            default: false
        })
    }
}, function(module) {
    module.on("enable", function() {
        module.tag = "NewTag";

        if (module.settings.myBooleanSetting.get()) {
            Chat.print("The module is now enabled.");
            module.settings.myBooleanSetting.set(false);
        }
    });
});
```