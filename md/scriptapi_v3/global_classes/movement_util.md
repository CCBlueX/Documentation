## MovementUtil

Provides various methods related to player movement.

### Method summary

#### `MovementUtil.getSpeed(): float`
Returns the speed the player is moving at.

#### `MovementUtil.isMoving(): boolean`
Returns whether the player is moving.

#### `MovementUtil.strafe(): void`
Makes the player strafe.

#### `MovementUtil.strafeWithSpeed(speed: float): void`
Makes the player strafe with a given speed. \
List of parameters:
- `speed`, the in-air speed of the player while strafing.

#### `MovementUtil.strafeWithStrength(strength: float): void`
Makes the player strafe with a given strength. \
List of parameters:
- `strength`, the stremgth to strafe with.

#### `MovementUtil.strafeWithSpeedAndStrength(speed: float, strength: float): void`
Combination of `MovementUtil::strafeWithSpeed` and `MovementUtil::strafeWithStrength`. \
List of parameters:
- `speed`, the in-air speed of the player while strafing.
- `strength`, the stremgth to strafe with.