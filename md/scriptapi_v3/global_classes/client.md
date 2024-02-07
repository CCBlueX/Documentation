## Client

The Client class provides various methods to facilitate interaction with the client.

### Method summary

#### `Client.displayChatMessage(message: string): void`
Prints the given *message* to the chat locally. It is not sent to the server. <br>
List of parameters:
- *message*, the message to print.

### Field summary

#### `Client.eventManager`
Manages game events. See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/event/EventManager.kt) for more information.

### `Client.configSystem`
Manages client configurations. See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/config/ConfigSystem.kt) for more information.

### `Client.moduleManager`
Manages modules (cheats). See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/features/module/ModuleManager.kt) for more information.

**Examples:**

Retrieving a module from the module manager.
```js
const killAura = client.moduleManager.getModuleByName("KillAura");
```

Getting all available module categories.
```js
const categories = client.moduleManager.getCategories(); // ["Movement", "Combat", "Render", ...]
```


### `Client.commandManager`
Manages client commands. See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/features/command/CommandManager.kt) for more information.

### `Client.scriptManager`
Manages installed scripts. See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/script/ScriptManager.kt) for more information.

### `Client.combatManager`
Manages rotations for combat. See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/utils/combat/CombatUtils.kt) for more information.