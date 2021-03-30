## Scripts
Each script has to be manually registered with the client before beginning to create modules, commands or inventory tabs. For this purpose the ScriptAPI has a global method to which some information about the script must also be passed. This method is `registerScript`.

### Registering a script
The first line of each script must specify the API version used. If this line is missing, the script will run with support for old API versions and new features may not work correctly. This is done with the help of the following, magic comment.
```js
/// api_version=2
```
#### registerScript(options)
This method can be used to register a script with the client. It returns the instance of this script, which should be stored in a global variable named `script`. All further methods for registering other components are defined on it. <br>
The following table describes the properties of the `options` object.

| Property | Description                                                         | Type   |
|----------|---------------------------------------------------------------------|--------|
| name     | Name of the script.                                                 | string |
| version  | Current version of this script.                                     | string |
| authors  | Array containing the name of everyone who has worked on the script. | array  |
Example:
```js
/// api_version=2
var script = registerScript({
    name: "My Script",
    version: "1.0.0",
    authors: ["CCBlueX", "Axolotls"]
});
```

### Handling events
Similar to script modules, the script instance also has its own events. These events therefore relate to the entire script. <br>
The general syntax of an event handler is as follows:
```js
script.on(eventName, function() {

});
```
The following events are available:

| Event Name | Description                                                                             |
|------------|-----------------------------------------------------------------------------------------|
| load       | Called when the script is loaded by the client. Not called when the client is reloaded. |
| enable     | Called when the script is enabled by the client.                                        |
| disable    | Called when the script is disabled by the client.                                       |
Example:
```js
script.on("load", function() {
    Chat.print("Script is now enabled!");
});
```

### Methods defined on `script`
#### script.import(path)
Imports another script file into the context of this script. It can be used to split up the project into multiple files containing different logic.
List of arguments:
- path, path to the file to import (relative to the file from which `import` is called).

---

#### script.registerModule(object, callback)
Refer to the documentation on registering a script module. It can be found [here](/docs/ScriptAPI/Creating%20Modules/Overview).

---

#### script.registerCommand(object, callback)
Refer to the documentation on registering a script command. It can be found [here](/docs/ScriptAPI/Creating%20Commands).

---

#### script.registerTab(object)
Refer to the documentation on registering an inventory tab. It can be found [here](/docs/ScriptAPI/Creating%20Inventory%20Tabs).

### Full script examples
A lot of in-depth examples on how to use the script API can be found in [this](https://github.com/CCBlueX/LiquidBounce-ScriptAPI/tree/master/examples) GitHub repository.