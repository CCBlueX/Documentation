## Client

The Client class provides various methods to facilitate interaction with the client.

### Method summary

#### `Client.displayChatMessage(message: string): void`
Prints the given *message* to the chat locally. It is not sent to the server. <br>
List of parameters:
- *message*, the message to print.

### Field summary

### `Client.eventManager`
Manages game events. See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/event/EventManager.kt) for more information.

<hr>

### `Client.configSystem`
Manages client configurations. See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/config/ConfigSystem.kt) for more information.

<hr>

### `Client.moduleManager`
Manages modules (cheats). See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/features/module/ModuleManager.kt) for more information.

**Example:**

Retrieving a module from the module manager (the name is not case-sensitive).
```js
const killAura = Client.moduleManager.get("KillAura");
```

<hr>

### `Client.commandManager`
Manages client commands. See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/features/command/CommandManager.kt) for more information.

<hr>

### `Client.scriptManager`
Manages installed scripts. See [GitHub](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/main/src/main/kotlin/net/ccbluex/liquidbounce/script/ScriptManager.kt) for more information.

<hr>

### `Client.combatManager`
Tracks combat state, such as whether the player is fighting. See [GitHub](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/utils/combat/CombatManager.kt) for more information.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptClient.kt)*
