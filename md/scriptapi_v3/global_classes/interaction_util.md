## InteractionUtil

The InteractionUtil class provides various methods for interacting with the environment.

### Method summary

#### `InteractionUtil.attackEntity(entity: Entity, swing: boolean, keepSprint: boolean): void`
Attempts to attack the given entity. Does nothing if *entity* is the player. <br>
List of parameters:
- *entity*, the entity to attack.
- *swing*, whether to swing the player's hand when attacking.
- *keepSprint*, whether to keep sprinting while attacking.

<hr>

#### `InteractionUtil.interactEntity(entity: Entity, hitResult: EntityHitResult, hand: InteractionHand): void`
Attempts to interact with the given entity. Does nothing if *entity* is the player. <br>
List of parameters:
- *entity*, the entity to interact with.
- *hitResult*, the hit result describing where the entity is clicked.
- *hand*, the hand to use to interact with the entity (main hand or off hand).

<hr>

#### `InteractionUtil.useItem(hand: InteractionHand): void`
Uses the item currently in the given hand. <br>
List of parameters:
- *hand*, the hand holding the item to use (main hand or off hand).

<hr>

#### `InteractionUtil.placeBlock(blockPos: BlockPos, hand: InteractionHand): boolean`
Attempts to place the block in the given hand at the given *BlockPos*. Returns whether the block was placed. <br>
List of parameters:
- *blockPos*, the position to place the block at.
- *hand*, the hand holding the block to place (main hand or off hand).

**Example:**

```js
InteractionUtil.useItem(InteractionHand.MAIN_HAND);
```

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce-Addon-ScriptAPI/blob/143f553/src/main/kotlin/net/ccbluex/liquidbounce/script/bindings/api/ScriptInteractionUtil.kt)*
