## Introduction

LiquidBounce's script API is based on [GraalJS](https://github.com/oracle/graaljs), an *ECMAScript 2023 compliant JavaScript implementation built on [GraalVM](https://www.graalvm.org)*. GraalVM's [polyglot functionality](https://www.graalvm.org/latest/reference-manual/polyglot-programming/) lets scripts written in JavaScript work directly with the client, which is written in Java and Kotlin. Scripts can use Java's and Minecraft's classes, methods and fields, so this will feel familiar if you have written Minecraft mods before. Scripts need the [Script API add-on](/docs/script-api/installation).

## Getting started with development

To begin, create a new file with a `.js` or `.mjs` extension (for example, `my_script.mjs`) and open it in your preferred code editor (such as [Visual Studio Code](https://code.visualstudio.com/)). This file will contain all the code covered in this introduction. The script we are going to write will introduce a new module that prints a string to the chat upon activation and a client command that adds two numbers.

Minecraft's classes, methods and fields use their Mojang names, which you can browse on [mappings.dev](https://mappings.dev/).

### Registering the script

The first thing every script must do is register itself with the client providing it with its name, version and information about its authors. Invoking `registerScript` will also return a new script instance on which modules and commands can be registered. While you may use an arbitrary string for the version number, adhering to the [Semver](https://semver.org/) standard is highly recommended.

```js
const script = registerScript({
  name: "MyScript",
  version: "1.0.0",
  authors: ["My Name"]
});
```

### Creating a new module

When registering a new module, some information must be provided, which is then displayed in LiquidBounce's GUIs. The required details include a name, a description, and a category under which the module should appear in the client's ClickGUI. For more information on supported details and a list of all available categories, see [Creating Modules](/docs/script-api/creating-modules/overview).

Our module will be called *MyModule* and will belong to the *Misc* category. Add the following code to your script file to register it.

```js
script.registerModule({
  name: "MyModule",
  category: "Misc", // Movement, Combat, Render, ...
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

The API supports many more events. The most commonly used events are:
- `enable`: Called whenever the module is enabled.
- `disable`: Called whenever the module is disabled.
- `playerTick`: Called once every game tick while you are in a world (~20 times per second).

The full list of supported events can be found [here](https://github.com/CCBlueX/LiquidBounce/tree/main/src/main/kotlin/net/ccbluex/liquidbounce/event/events).

All event handlers can be `async` functions (including `enable` and `disable`), see [AsyncUtil](/docs/script-api/global-classes/asyncutil).
A `Promise` in JavaScript cannot be cancelled (unlike Kotlin's `Job` or Java's `Future`), so check whether your module is still enabled after each `await`.

### Creating a command

Another way of introducing new functionality is through client commands. Commands usually accept arguments, process them in some way and then perform an action once. Unlike modules, they are not intended to run for extended periods of time.

Similarly to modules, commands have to be registered with the client. The code shown below will introduce a new command called *addition* or *add* which accepts two integer parameters, adds them and prints them to the chat. The `validate` function can be used to ensure a parameter adheres to certain rules. In this case, it must be an integer. `ParameterValidator.integer` will also convert the parameter to an integer, so we don't have to manually parse it in `onExecute`. For more information on parameter validation, see [ParameterValidator](/docs/script-api/global-classes/parametervalidator).

```js
script.registerCommand({
  name: "addition",
  aliases: ["add"],
  parameters: [{
      name: "a",
      required: true,
      validate: ParameterValidator.integer
    },
    {
      name: "b",
      required: true,
      validate: ParameterValidator.integer
    }
  ],
  onExecute(arg1, arg2) {
    Client.displayChatMessage(`Result of ${arg1} + ${arg2} is ${arg1 + arg2}`);
  }
});
```

For more details on command creation, see [Creating Commands](/docs/script-api/creating-commands).

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
  parameters: [{
      name: "a",
      required: true,
      validate: ParameterValidator.integer
    },
    {
      name: "b",
      required: true,
      validate: ParameterValidator.integer
    }
  ],
  onExecute(arg1, arg2) {
    Client.displayChatMessage(`Result of ${arg1} + ${arg2} is ${arg1 + arg2}`);
  }
});
```

To run the script, place it inside the *scripts* directory located in the *LiquidBounce* directory which in turn can be found in the *.minecraft* directory of your installation. When using LiquidLauncher, simply press the directory icon with the arrow in the top right corner next to the *Data location* field in the launcher's settings window to open the data directory in your file manager. You can also open the folder in game with `.script browse`, and load a new script with `.script reload` without restarting. Then open a singleplayer world and open the ClickGUI. You should find *MyModule* in the *Misc* category and sending *.addition 1 2* into the chat should execute your command and yield *3* as a result.

## Additional documentation

There is [Dokka documentation](https://ccbluex.github.io/LiquidBounce/) for the client. Call its methods the way you would from Java. Kotlin `suspend` functions cannot be called from JavaScript.

## Examples

Example scripts are in the [examples folder](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/tree/main/examples) of the Script API add-on.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/PolyglotScript.kt)*
