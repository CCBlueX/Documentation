## BlockUtil

The BlockUtil class provides various methods for working with blocks and block positions.

### Method summary

#### `BlockUtil.newBlockPos(x: int, y: int, z: int): BlockPos`
Creates a new *BlockPos* for the given coordinates. <br>
List of parameters:
- *x*, x coordinate of the position.
- *y*, y coordinate of the position.
- *z*, z coordinate of the position.

<hr>

#### `BlockUtil.getBlock(blockPos: BlockPos): Block`
Returns the *Block* at the given *BlockPos*. <br>
List of parameters:
- *blockPos*, the position to get the block at.

<hr>

#### `BlockUtil.getState(blockPos: BlockPos): BlockState`
Returns the *BlockState* of the block at the given *BlockPos*, or `null` if no world is loaded. <br>
List of parameters:
- *blockPos*, the position of the block to get the state of.

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptBlockUtil.kt)*
