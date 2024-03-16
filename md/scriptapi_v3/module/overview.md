## Creating Modules

Modules can be toggled from either the user interface or through the *toggle* command. Unlike commands which perform an action once, modules may run indefinitely and listen for and react to relevant events.

### Registering a module

Calling the `registerModule` on your scripts instance will register a module with the client.

```js
script.registerModule(options, callback);
```

The object passed to `registerModule` may contain the following options:

| Propery     | Description                                                                                                               | Required | Type   | Default |
|-------------|---------------------------------------------------------------------------------------------------------------------------|----------|--------|---------|
| name        | Name of the module.                                                                                                       | Yes      | string |         |
| category    | Category of the module.                                                                                                   | Yes      | string |         |
| description | A description of what the module does.                                                                                    | No       | string | ""      |
| tag         | Additional text displayed next to the module name in the ArrayList. May be used to display the current mode, for example. | No       | string | ""      |
| settings    | An object containing the settings of the module.                                                                          | No       | object | {}      |

`category` may be one of thw following:
- Client
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

Settings can be used to allow the user to adjust the module's behavior to their needs. LiquidBounce's script API offers many different types of settings fulfilling differtent purposes. Each setting must be passed to `registerModule` in the `settings` object. The settings key represents the internal name of the setting under which it can later be accessed in your code.

For a full list of available settings, click [here](/docs/Script%20API/Global%20Classes/Setting).

#### Events

Modules may react to certain situations by listening for events. An event listener can be registered by passing its name alongside a callback function to the `on` method of a module's instance.

Common events are:
- `enable`, called when the module is enabled.
- `disable`, called when the module is disabled.
- `tick`, called when a game tick is processed (~20 times per second).
- `packet`, called when a network packet is being processed.
- `key`, called when a keyboard key is being pressed.

Many events also pass a payload containg additional information about the event.

**Example:** Registering a module that prints a chat message when its boolean setting is enabled and the name of a key being pressed.

```js
script.registerModule({
    name: "MyModule",
    category: "Misc",
    description: "Just a demonstration.",
    settings: {
        myBooleanSetting: Setting.boolean("MySetting", true)
    }
}, mod => {
    mod.on("enable", () => {
        if (mod.settings.myBooleanSetting.value) {
            Client.displayChatMessage("MySetting is true!");
        }
    });

    mod.on("key", event => {
        Client.printChatMessage(`${event.getKey().getTranslationKey()} has been pressed.`);
    });
});
```

For a full list of supported events and their attributes, click [here](https://github.com/CCBlueX/LiquidBounce/tree/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/event/events).