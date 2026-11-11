## RotationUtil

The RotationUtil class provides various methods to facilitate the creation of rotations.

### Method summary

#### `RotationUtil.newRaytracedRotationEntity(entity: Entity, range: double, throughWallsRange: double): Rotation`
Returns the optimal rotation for facing the given entity, or `null` if no point of it can be hit. It uses raytracing so if performance is a concern, using `newRotationEntity` is recommended instead. <br>
List of parameters:
- *entity*, the entity to face.
- *range*, the squared maximum distance the entity can be away to still face it (pass `9` for 3 blocks).
- *throughWallsRange*, the maximum distance through walls in blocks (not squared).

<hr>

#### `RotationUtil.newRotationEntity(entity: Entity): Rotation`
Returns the rotation needed to face the center of the given entity's bounding box. <br>
List of parameters:
- *entity*, the entity to face.

<hr>

#### `RotationUtil.aimAtRotation(rotation: Rotation, fixVelocity: boolean): void`
Applies the given rotation to the player through the client's rotation manager. <br>
List of parameters:
- *rotation*, the rotation to apply.
- *fixVelocity*, whether to correct the player's movement to match the rotation, which some anti-cheats require.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptRotationUtil.kt)*
