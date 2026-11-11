# Movement with Baritone

## Go to Specific Coordinates

<video src="/images/baritone/commands/goto.mp4" controls width="600">Your browser does not support the video tag.</video>

```
#goto x y z
```
or just
```
#goto x z
```

For example, `#goto 100 64 -200` walks you to those coordinates.

## Path in the Direction You're Facing

<video src="/images/baritone/commands/thisway.mp4" controls width="600">Your browser does not support the video tag.</video>

```
#thisway 1000
```

Baritone travels 1000 blocks in the direction you are looking.

## Explore Around You

```
#explore x z
```

Explores the world, starting from the point x, z.

## Waypoint System

```
#wp
```

Lists all waypoint commands.

```
#wp save user home
```

Saves your current position as a waypoint called "home" under the "user" tag.

```
#wp goal home
```

Sets your goal to the "home" waypoint.
