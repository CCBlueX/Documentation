## Creating Modules

Modules can be toggled from either the user interface or through the *toggle* command. Unlike commands which perform an action once, modules may run indefinitely and listen for and react to relevant events.

### Registering a module

Calling `registerModule` on your script's instance will register a module with the client.

```js
script.registerModule(options, callback);
```

The object passed to `registerModule` may contain the following options:

| Property    | Description                                                                                                               | Required | Type   | Default |
|-------------|---------------------------------------------------------------------------------------------------------------------------|----------|--------|---------|
| name        | Name of the module.                                                                                                       | Yes      | string |         |
| category    | Category of the module.                                                                                                   | Yes      | string |         |
| description | A description of what the module does.                                                                                    | No       | string | ""      |
| tag         | Additional text displayed next to the module name in the ArrayList. May be used to display the current mode, for example. Can be changed later through `mod.tag`. | No       | string |         |
| settings    | An object containing the settings of the module.                                                                          | No       | object | {}      |

`category` may be one of the following:
- Combat
- Exploit
- Fun
- Misc
- Movement
- Player
- Render
- World

The argument passed to the `callback` function contains the instance of the module you registered.

#### Settings

Settings can be used to allow the user to adjust the module's behavior to their needs. LiquidBounce's script API offers several types of settings. Each setting must be passed to `registerModule` in the `settings` object. The key of each entry is the internal name of the setting under which it can later be accessed in your code.

For a full list of available settings, see [Setting](/docs/script-api/global-classes/setting).

#### Events

Modules may react to certain situations by listening for events. An event listener can be registered by passing its name alongside a callback function to the `on` method of a module's instance.

Common events are:
- `enable`, called when the module is enabled.
- `disable`, called when the module is disabled.
- `gameTick`, called when a game tick is processed (~20 times per second).
- `packet`, called when a network packet is sent or received.
- `key`, called when a key is pressed or released.

Many events also pass a payload containing additional information about the event. If a handler throws an error, the module is turned off and the error is shown in chat.

**Example:** Registering a module that prints a chat message when its boolean setting is enabled, and the name of every key pressed.

```js
script.registerModule({
    name: "MyModule",
    category: "Misc",
    description: "Just a demonstration.",
    settings: {
        myBooleanSetting: Setting.boolean({
            name: "MySetting",
            default: true
        })
    }
}, mod => {
    mod.on("enable", () => {
        if (mod.settings.myBooleanSetting.value) {
            Client.displayChatMessage("MySetting is true!");
        }
    });

    mod.on("key", event => {
        Client.displayChatMessage(`${event.getKey().getName()} has been pressed.`);
    });
});
```

For a full list of supported events and their attributes, see the [event classes](https://github.com/CCBlueX/LiquidBounce/tree/main/src/main/kotlin/net/ccbluex/liquidbounce/event/events).

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/features/ScriptModule.kt)*
