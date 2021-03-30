## mc
`mc` contains the Minecraft instance (`Minecraft.getMinecraft()`) It is the most important instance in every script. It can be used to do almost any manipulation desired to the game. Instead of listing all available methods and fields here, we refer to the Minecraft JavaDocs, which can also be found online [here](https://scriptapi.liquidbounce.net).

## moduleManager
The ModuleManager is, as the name suggests, responsible for managing all registered modules. With it new modules can be registered and already existing ones can be unregistered. Furthermore it is possible to retrieve instances of modules to be able to perform further actions on them. Only the most important methods are listed here. To view all methods, please refer to the [source code](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/features/module/ModuleManager.kt) of the class on Github.

### Method summary
#### moduleManager.getModule(name)
Returns the instance of [Module](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/features/module/Module.kt) with the given name. If a module with the given name is not found, `null` is returned. <br>
List of arguments:
- name, name of the module.

Example:
```js
// Changing the value of a setting defined on another module
moduleManager.getModule("KillAura").getValue("Range").set(3.4);

// Getting the value of a setting defined on another module
moduleManager.getModule("Scaffold").getValue("AutoBlock").get();
```

---

#### moduleManager.getModule()
Returns a List of all registered modules.

---

#### moduleManager.registerModule(module)
Registers the given module instance with the ModuleManager. Usually the script API does this automatically. <br>
List of arguments:
- module, instance of the module to be registered.

---

#### moduleManager.unregisterModule(module)
Unregisters the given module. <br>
List of arguments:
- module, instance of the module to be unregistered.

## commandManager
Similar to the ModuleManager, the CommandManager takes over the task of managing commands. For this reason, similar methods are also defined on it. Again, only the most important methods are listed here, all of them can be viewed [here](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/features/command/CommandManager.kt).

### Method summary
#### commandManager.executeCommands(command)
Executes the given command.
<br>
List of arguments:
- command, string containing the command to be executed.

Example:
```js
commandManager.executeCommands(".killaura range 3.4");
```

---

#### commandManager.getCommand(name)
Returns an instance of [Command](https://github.com/CCBlueX/LiquidBounce/blob/master/1.8.9-Forge/src/main/java/net/ccbluex/liquidbounce/features/command/Command.kt) with the given name. If a command with the given name is not found, `null` is returned. <br>
List of arguments:
- name, name of the command.

---

#### commandManager.registerCommand(command)
Registers the given command instance with the CommandManager.
List of arguments:
- command, instance of the command to be registered.

---

#### commandManager.unregisterCommand(module)
Unregisters the given command. <br>
List of arguments:
- command, instance of the command to be unregistered.