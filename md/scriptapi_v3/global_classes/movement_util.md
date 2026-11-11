## MovementUtil

Provides various methods related to player movement.

### Method summary

#### `MovementUtil.getSpeed(): double`
Returns the player's horizontal speed.

<hr>

#### `MovementUtil.isMoving(): boolean`
Returns whether the player is moving.

<hr>

#### `MovementUtil.strafe(): void`
Makes the player strafe.

<hr>

#### `MovementUtil.strafeWithSpeed(speed: double): void`
Makes the player strafe with a given speed. <br>
List of parameters:
- *speed*, the in-air speed of the player while strafing.

<hr>

#### `MovementUtil.strafeWithStrength(strength: double): void`
Makes the player strafe with a given strength. <br>
List of parameters:
- *strength*, the strength to strafe with.

<hr>

#### `MovementUtil.strafeWithSpeedAndStrength(speed: double, strength: double): void`
Combination of *MovementUtil::strafeWithSpeed* and *MovementUtil::strafeWithStrength*. <br>
List of parameters:
- *speed*, the in-air speed of the player while strafing.
- *strength*, the strength to strafe with.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptMovementUtil.kt)*
