## BlockUtil

The BlockUtil class provides various methods for working with blocks and block posiotions.

### Method summary

#### `BlockUtil.newBlockPos(x: int, y: int, z: int): BlockPos`
Creates a new `BlockPos` for the given coordinates. <br>
List of parameters:
- `x`, x coordinate of the position.
- `y`, y coordinate of the position.
- `z`, z coordinate of the position.

#### `BlockUtil.getBlock(blockPos: BlockPos): Block`
Returns the `Block` at the given `BlockPos`. <br>
List of parameters:
- `blockPos`, the position to get the block at.

#### `BlockUtil.getState(blockPos: BlockPos): BlockState`
Returns the `BlockState` of the block at the given `BlockPos`. <br>
List of parameters:
- `blockPos`, the position of the block to get the state of.
