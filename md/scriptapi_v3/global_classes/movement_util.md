## MovementUtil

Provides various methods related to player movement.

### Method summary

#### `MovementUtil.getSpeed(): float`
Returns the speed the player is moving at.

<hr>

#### `MovementUtil.isMoving(): boolean`
Returns whether the player is moving.

<hr>

#### `MovementUtil.strafe(): void`
Makes the player strafe.

<hr>

#### `MovementUtil.strafeWithSpeed(speed: float): void`
Makes the player strafe with a given speed. <br>
List of parameters:
- *speed*, the in-air speed of the player while strafing.

<hr>

#### `MovementUtil.strafeWithStrength(strength: float): void`
Makes the player strafe with a given strength. <br>
List of parameters:
- *strength*, the stremgth to strafe with.

<hr>

#### `MovementUtil.strafeWithSpeedAndStrength(speed: float, strength: float): void`
Combination of *MovementUtil::strafeWithSpeed* and *MovementUtil::strafeWithStrength*. <br>
List of parameters:
- *speed*, the in-air speed of the player while strafing.
- *strength*, the stremgth to strafe with.