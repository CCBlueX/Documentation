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
Lets Baritone walk up diagonally (default: false). This is fairly safe.

```
allowDiagonalDescend
```
Lets Baritone walk down diagonally (default: false). This is a bit risky, because it can touch blocks it didn't check.

```
followRadius
```
Sets how close Baritone will stay to the entity it's following (default: 3).

## Mining Settings

```
legitMine
```
Only mines ores you can see, so mining looks more like a normal player (default: false).

```
mineScanDroppedItems
```
Picks up dropped items while mining (default: true).

## Building Settings

```
buildInLayers
```
Builds one layer at a time and finishes it before starting the next (default: false).

```
backfill
```
Fill in blocks behind you while tunneling (default: false).

## Collection Settings

```
acceptableThrowawayItems
```
Blocks Baritone may use up, for example for bridging. By default:
- Dirt
- Cobblestone
- Netherrack
- Stone

## World Interaction

```
blocksToAvoidBreaking
```
Blocks Baritone only breaks when it has no other way. By default:
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
- Change a setting with `#set <setting> <value>`, for example `#set allowSprint false`
- Your changes are saved in `baritone/settings.txt`
- `#modified` lists the settings you changed
- `#reset` puts all settings back to default
- Type `#help set` in the game for more
