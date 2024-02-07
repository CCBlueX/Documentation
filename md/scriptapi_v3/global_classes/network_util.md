## NetworkUtil

The NetworkUtil class provides various methods to facilitate interaction with Minecraft's networking features.

### Method summary

#### `NetworkUtil.movePlayerGround(onGround: boolean): void`
Sends an *PlayerMoveC2SPacket.OnGroundOnly* packet. <br>
List of parameters:
- *onGround*, whether movement if on ground only.

<hr>

#### `NetworkUtil.movePlayerPosition(x: float, y: float, z: float, onGround: boolean): void`
Sends an *PlayerMoveC2SPacket.PositionAndOnGround* packet. <br>
List of parameters:
- *x*, x position to move to.
- *y*, y position to move to.
- *z*, z position to move to.
- *onGround*, whether movement if on ground only.

<hr>

#### `NetworkUtil.movePlayerPositionAndLook(x: float, y: float, z: float, yaw: float, pitch: float, onGround: boolean): void`
Sends an *PlayerMoveC2SPacket.Full* packet. <br>
List of parameters:
- *x*, x position to move to.
- *y*, y position to move to.
- *z*, z position to move to.
- *yaw*, yaw position of the player's head.
- *pitch*, pitch position of the player's head.
- *onGround*, whether movement if on ground only.

<hr>

#### `NetworkUtil.movePlayerLook(yaw: float, pitch: float, onGround: boolean): void`
Sends an *PlayerMoveC2SPacket.LookAndOnGround* packet. <br>
List of parameters:
- *yaw*, yaw position of the player's head.
- *pitch*, pitch position of the player's head.
- *onGround*, whether movement if on ground only.

<hr>

#### `NetworkUtil.sendChatMessage(message: string): void`
Sends a chat message to the server. <br>
List of parameters:
- *message*, the message to send.

<hr>

#### `NetworkUtil.sendCommand(command: String): void`
Executes a server command. <br>
List of parameters:
- *command*, the command to execute.