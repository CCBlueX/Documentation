# Baritone Settings

## The Essentials

```
allowBreak
```
Toggles whether Baritone can break blocks (default: true).

```
allowSprint
```
Toggles whether Baritone can sprint (default: true).

```
allowPlace
```
Toggles whether Baritone can place blocks (default: true).

```
allowParkour
```
Toggles whether Baritone can perform parkour jumps (default: false).

```
allowParkourPlace
```
Toggles whether Baritone can place blocks during parkour (default: false).

```
blockPlacementPenalty
```
How much to penalize block placement. Higher values make Baritone less likely to place blocks (default: 20.0).

## Pathfinding Settings

```
allowDiagonalAscend
```
Allow diagonal ascending (default: false). Actually quite safe compared to diagonal descend.

```
allowDiagonalDescend
```
Allow descending diagonally (default: false). Slightly unsafe, can contact unchecked blocks.

```
followRadius
```
Sets how close Baritone will stay to the entity it's following (default: 3).

## Mining Settings

```
legitMine
```
Makes mining look more "legitimate" by only mining blocks you can see (default: false).

```
mineScanDroppedItems
```
Determines if Baritone will target dropped items while mining (default: true).

## Building Settings

```
buildInLayers
```
Don't consider the next layer in builder until the current one is done (default: false).

```
backfill
```
Fill in blocks behind you while tunneling (default: false).

## Collection Settings

```
acceptableThrowawayItems
```
Blocks that Baritone is allowed to place (as throwaway, for bridging etc). Default includes:
- Dirt
- Cobblestone
- Netherrack
- Stone

## World Interaction

```
blocksToAvoidBreaking
```
Blocks that baritone shouldn't break unless necessary. Default includes:
- Crafting Table
- Furnace
- Chest
- Trapped Chest

## Performance Settings

```
renderGoal
```
Toggles rendering of the goal (default: true).

```
renderPath
```
Toggles rendering of the path (default: true).

## Additional Resources
- For a complete list of settings, use the `#help` command in-game
- Settings can be modified directly in `baritone/settings.txt`
- Use `modified` command to see all changed settings
- Use `reset` command to restore defaults
