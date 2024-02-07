## InteractionUtil

The InteractionUtil class provides various methods for interacting with the environment.

### Method summary

#### `InteractionUtil.attackEntity(entity: Entity, swing: boolean, keepSprint: boolean): void`
Attempts to attack the given entity. <br>
List of parameters:
- *entity*, the entity to attack.
- *swing*, whether to swing the players hand when attacking.
- *keepSpring*, whether to keep sprinting while attacking.

<hr>

#### `InteractionUtil.interactEntity(entity: Entity, hand: Hand): void`
Attempts to interact with the given entity. <br>
List of parameters:
- *entity*, the entity to interact with.
- *hand*, the hand to use to interact with the entity (main hand or off hand).

<hr>

#### `InteractionUtil.useItem(hand: Hand): void`
Uses the item currently in the given hand. <br>
List of parameters:
- *hand*, the hand holding the item to use (main hand or off hand).

<hr>

#### `InteractionUtil.placeBlock(blockPos: BlockPos, hand: Hand): boolean`
Attempts to place the block in the given *Hand* at the given *BlockPos*. Returns whether the block was successfully places. \
List of parameters:
- *blockPos*, the position to place the block at.
- *hand*, the hand holding the block to place (main hand or off hand).