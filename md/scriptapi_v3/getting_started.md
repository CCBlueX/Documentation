## Introduction

LiquidBounce's script API is based on [GraalJS](https://github.com/oracle/graaljs), an *ECMAScript 2023 compliant JavaScript implementation built on [GraalVM](https://www.graalvm.org)*. GraalVM's [polyglot functionality](https://www.graalvm.org/latest/reference-manual/polyglot-programming/) enables saemless interoperation between scripts written in JavaScript and the client written in Java and Kotlin. This integration facilitates easy access and utilization of Java's and Minecraft's classes, methods, and fields, making development particularly intuitive for those already familiar with Minecraft modding.

## Getting started with development

To begin, create a new file with a `.mjs` extension (for example, `my_script.mjs`) and open it in your preferred code editor (such as [Visual Studio Code](https://code.visualstudio.com/)). This file will encompass  the entire code covered in this introduction. The script we are going to write will introduce a new module that prints a string to the chat upon activation and a client command that adds two numbers.

Documentation of classes, methods and fields of the Minecraft client can be found [here](https://maven.fabricmc.net/docs/yarn-1.20.4+build.3/index.html).

### Registering the script

The first thing every script should do is registering itself with the client providing it with its name, version and information about its authors. Invoking `registerScript` will also return a new script instance on which modules and commands can be registered. While you may use an arbitrary string the version number, adhering to the [Semver](https://semver.org/) standard is highly recommended.

```js
const script = registerScript({
    name: "MyScript",
    version: "1.0.0",
    authors: ["My Name"]
});
```

### Creating a new module

When registering a new module, some information must be provided, which is then displayed in LiquidBounce's GUIs. The required details include a name, a description, and a category under which the module should appear in the client's ClickGUI / TabGUI. For more information on supported details and a list of all available categories, click [here](#). TODO

Our module will be called *MyModule* and will belong to the *Misc* category. Add the following code to your script file to register it.

```js
script.registerModule({
    name: "MyModule",
    category: "Misc", // Movement, Combat, Renderr, ...
    description: "An example module created with LiquidBounce's script API."
}, (mod) => {

});
```

The argument passed to `registerModule`'s callback function contains the instance of the module that was registered. If we ran the client now, we would find our module in the *Misc* category but enabling it wouldn't do anything yet.

### Listening for events

To actually make our module do something, we have to start listening for events and in some way react to them. In our case, we will listen for the `enable` event, which is called whenever the module is enabled. We want the module to print something to the chat, so we call `Client.displayChatMessage`, a method provided by the API.

```js
mod.on("enable", () => {
    Client.displayChatMessage("§aAxolotls are great!");
});
```

Now, every time we enable our module, *Axolotls are great!* will be displayed in the chat (It will not be sent to the server).

A plethora of additional events are supported by the API and serve different purposes. The most commonly used events are:
- `enable`: Called whenever the module is enabled.
- `disable`: Called whenever the module is disabled.
- `playerTick`: Called once every game tick (~20 times per second).

The full list of supported events can be found [here](#). TODO

### Creating a command

Another way of introducing new functionality is through client commands. Commands usually accept arguments, process them in some way and then perform an action once. Unlike modules, they are not intended to run for extended periods of time.

Similarly to modules, commands have to be registered with the client. The code shown below will introduce a new command called *addition* or *add* which accepts two integer parameters, adds them and prints them to the chat.

```js
script.registerCommand({
    name: "addition",
    aliases: ["add"],
    parameters: [
        {
            name: "name",
            required: true,
        },
        {
            name: "local",
            required: true,
        }
    ],
    onExecute(arg1, arg2) {
        const a = parseInt(arg1);
        const b = parseInt(arg2);
        Client.displayChatMessage(`Result of ${a} + ${b} is ${a + b}`);
    }
});
```

For more details on command creation, click [here](#). TODO


### Final script

Here is the full code of the script we just wrote:

```js
const script = registerScript({
    name: "MyScript",
    version: "1.0.0",
    authors: ["My Name"]
});

script.registerModule({
    name: "MyModule",
    category: "Misc", // Movement, Combat, Render, ...
    description: "An example module created with LiquidBounce's script API."
}, (mod) => {
    mod.on("enable", () => {
        Client.displayChatMessage("§aAxolotls are great!");
    });
});

script.registerCommand({
    name: "addition",
    aliases: ["add"],
    parameters: [
        {
            name: "name",
            required: true,
        },
        {
            name: "local",
            required: true,
        }
    ],
    onExecute(arg1, arg2) {
        const a = parseInt(arg1);
        const b = parseInt(arg2);
        Client.displayChatMessage(`Result of ${a} + ${b} is ${a + b}`);
    },
});
```

To run the script, place it inside the *scripts* directory located in the *LiquidBounce* directory which in turn can be found in the *.minecraft* directory of your installation. When using LiquidLauncher, simply press the directory icon with the arrow in the top right corner next to the *Data location* field in the launcher's settings window to open the data diretory in your file manager. Once you ran the game, open up a single player world and open the ClickGUI. You should find *MyModule* in the *Misc* category and sending *.addition 1 2* into the chat should execute your command and yield *3* as a result.

## Examples
A repository with additional examples can be found on our [GitHub page](https://github.com/CCBlueX/LiquidScript).
