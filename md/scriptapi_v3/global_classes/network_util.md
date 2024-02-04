## NetworkUtil

The NetworkUtil class provides various methods to facilitate interaction with Minecraft's networking features.

### Method summary

#### `NetworkUtil.movePlayerGround(onGround: boolean): void`
Sends an `PlayerMoveC2SPacket.OnGroundOnly` packet. \
List of parameters:
- `onGround`, whether movement if on ground only.

#### `NetworkUtil.movePlayerPosition(x: float, y: float, z: float, onGround: boolean): void`
Sends an `PlayerMoveC2SPacket.PositionAndOnGround` packet. \
List of parameters:
- `x`, x position to move to.
- `y`, y position to move to.
- `z`, z position to move to.
- `onGround`, whether movement if on ground only.

#### `NetworkUtil.movePlayerPositionAndLook(x: float, y: float, z: float, yaw: float, pitch: float, onGround: boolean): void`
Sends an `PlayerMoveC2SPacket.Full` packet. \
List of parameters:
- `x`, x position to move to.
- `y`, y position to move to.
- `z`, z position to move to.
- `yaw`, yaw position of the player's head.
- `pitch`, pitch position of the player's head.
- `onGround`, whether movement if on ground only.

#### `NetworkUtil.movePlayerLook(yaw: float, pitch: float, onGround: boolean): void`
Sends an `PlayerMoveC2SPacket.LookAndOnGround` packet. \
List of parameters:
- `yaw`, yaw position of the player's head.
- `pitch`, pitch position of the player's head.
- `onGround`, whether movement if on ground only.

#### `NetworkUtil.sendChatMessage(message: string): void`
Sends a chat message to the server. \
List of parameters:
- `message`, the message to send.

#### `NetworkUtil.sendCommand(command: String): void`
Executes a server command. \
List of parameters:
- `command`, the command to execute.