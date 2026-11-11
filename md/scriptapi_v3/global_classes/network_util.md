## NetworkUtil

The NetworkUtil class provides various methods to facilitate interaction with Minecraft's networking features.

### Method summary

#### `NetworkUtil.movePlayerGround(onGround: boolean, horizontalCollision: boolean): void`
Sends a *ServerboundMovePlayerPacket.StatusOnly* packet. <br>
List of parameters:
- *onGround*, whether the player is on the ground.
- *horizontalCollision*, whether the player collides horizontally.

<hr>

#### `NetworkUtil.movePlayerPosition(x: double, y: double, z: double, onGround: boolean, horizontalCollision: boolean): void`
Sends a *ServerboundMovePlayerPacket.Pos* packet. <br>
List of parameters:
- *x*, x position to move to.
- *y*, y position to move to.
- *z*, z position to move to.
- *onGround*, whether the player is on the ground.
- *horizontalCollision*, whether the player collides horizontally.

<hr>

#### `NetworkUtil.movePlayerPositionAndLook(x: double, y: double, z: double, yaw: float, pitch: float, onGround: boolean, horizontalCollision: boolean): void`
Sends a *ServerboundMovePlayerPacket.PosRot* packet. <br>
List of parameters:
- *x*, x position to move to.
- *y*, y position to move to.
- *z*, z position to move to.
- *yaw*, yaw of the player's head.
- *pitch*, pitch of the player's head.
- *onGround*, whether the player is on the ground.
- *horizontalCollision*, whether the player collides horizontally.

<hr>

#### `NetworkUtil.movePlayerLook(yaw: float, pitch: float, onGround: boolean, horizontalCollision: boolean): void`
Sends a *ServerboundMovePlayerPacket.Rot* packet. <br>
List of parameters:
- *yaw*, yaw of the player's head.
- *pitch*, pitch of the player's head.
- *onGround*, whether the player is on the ground.
- *horizontalCollision*, whether the player collides horizontally.

<hr>

#### `NetworkUtil.sendChatMessage(message: string): void`
Sends a chat message to the server. <br>
List of parameters:
- *message*, the message to send.

<hr>

#### `NetworkUtil.sendCommand(command: string): void`
Executes a server command. <br>
List of parameters:
- *command*, the command to execute, without the leading slash.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptNetworkUtil.kt)*
