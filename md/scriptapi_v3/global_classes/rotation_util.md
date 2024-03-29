## RotationUtil

The InteractionUtil class provides various methods to facilitate the creation of rotations.

### Method summary

#### `RotationUtil.newRaytracedRotationEntity(entity: Entity, range: float, throughWallsRange: float): Rotation`
Returns the optimal rotation for facing the given entity. It uses raytracing so if performance is a concern, using `newRotationEntity` is recommended instead. <br>
List of parameters:
- *entity*, the entity to face.
- *range*, the maximum distance the entity can be away to still face it.
- *throughWallsRange*, the maximum distance through walls the entity can be away to still face it.

<hr>

#### `RotationUtil.newRotationEntity(entity: Entity): Rotation`
Returns the necessary rotation to face the given entity. <br>
List of parameters:
- *entity*, the entity to face.

<hr>

#### `RotationUtil.aimAtRotation(rotation: Rotation, fixVelocity: boolean): Rotation`
Applies the given rotation to the player. <br>
List of parameters:
- *rotation*, the rotation to apply.
- *fixVelocity*, applies fixes to the player's rotation required to bypass some anti cheats.