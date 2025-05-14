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

Example: `#goto 100 64 -200` will make your character navigate to those coordinates.

## Path in the Direction You're Facing

<video src="/images/baritone/commands/thisway.mp4" controls width="600">Your browser does not support the video tag.</video>

```
#thisway 1000
```

This tells Baritone to travel 1000 blocks in the direction you're currently looking.

## Explore Around You

```
#explore x z
```

Systematically explores the world from the origin point of x,z.

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
