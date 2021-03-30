## ScriptAPI commands
Commands created with the script API can be executed just like regular commands. Compared to modules, they are especially useful when a particular action is to be performed only once and not continuously.

### Creating a command
#### script.registerCommand(options, callback)
Each command has to be registered with the client via the instance of the script. This is done using the `registerCommand` method. It creates a new instance of [ScriptCommand](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/script/api/ScriptCommand.kt) and passes it to the callback function. <br>
The following table describes the properties of the `options` object.

| Property | Description                                         | Type   |
|----------|-----------------------------------------------------|--------|
| name     | Name of the command.                                | string |
| aliases  | Array containing alternative names for the command. | array  |
Example:
```js
script.registerCommand({
    name: "testCommand",
    aliases: ["demoCommand", "exampleCommand"]
}, function(command) {

});
```

### Handling execution
Commands have only one event: The execute event. It is called whenever the user executes the command using its name or one of its aliases. The execute event has to be registered with the client. The [ScriptCommand](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/script/api/ScriptCommand.kt) class has a method for this purpose.
### module.on("execute", callback)
Registers the use of an event with the client.
List of arguments:
- "execute", name of the only available event.
- callback, function called whenever the event occurs. To it the arguments of the command executed are passed.

Example:
```js
command.on("execute", function(args) {
    if (args.length > 1) {
        Chat.print(args[1]);
    }
});
```

### Full example of a command
```js
script.registerCommand({
    name: "testCommand",
    aliases: ["demoCommand", "exampleCommand"]
}, function(command) {
    command.on("execute", function(args) {
        if (args.length > 1) {
            Chat.print(args[1]);
        }
    });
});
```
