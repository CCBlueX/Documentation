# How to use Baritone

Baritone uses a command prefix system to distinguish its commands from regular chat. The default prefix is `#`, so all Baritone commands will start with this symbol (e.g., `#goal`, `#mine`, etc.).

> **Note:** You can use commands directly in chat. Be careful with typos, as they will be sent to public chat if you make mistakes.

## Basic Command Usage

<video src="/images/baritone/commands/usage.mp4" controls width="600">Your browser does not support the video tag.</video>

To use Baritone commands:
1. Open the Minecraft chat (default: press 'T' key)
2. Type a command starting with `#` 
3. Press Enter to execute

## Essential Commands

### Getting Help

![Help command](/images/baritone/commands/help.png)

```
#help
```

This command shows all available Baritone commands. It's interactive - you can click on commands to get more information.

### Movement Commands

#### Go to Specific Coordinates

<video src="/images/baritone/commands/goto.mp4" controls width="600">Your browser does not support the video tag.</video>

```
#goto x y z
```
or just
```
#goto x z
```

Example: `#goto 100 64 -200` will make your character navigate to those coordinates.

#### Path in the Direction You're Facing

<video src="/images/baritone/commands/thisway.mp4" controls width="600">Your browser does not support the video tag.</video>

```
#thisway 1000
```

This tells Baritone to travel 1000 blocks in the direction you're currently looking.

#### Follow Other Players or Entities

<video src="/images/baritone/commands/follow.mp4" controls width="600">Your browser does not support the video tag.</video>

```
#follow player PlayerName
```

Makes your character follow a specific player.

```
#follow players
```

Follows any players in range (useful combined with combat modules).

```
#follow entity sheep
```

Follows entities of a specific type.

### Mining Commands

#### Mine Specific Blocks

<video src="/images/baritone/commands/mine.mp4" controls width="600">Your browser does not support the video tag.</video>

```
#mine diamond_ore iron_ore
```

This instructs Baritone to search for and mine diamond ore or iron ore.

You can specify an amount:
```
#mine 64 diamond_ore
```

### Pickup Automation

<video src="/images/baritone/commands/pickup.mp4" controls width="600">Your browser does not support the video tag.</video>

```
#pickup minecraft:diamond
```

This will automatically pickup items around you.

### Farming Automation

<video src="/images/baritone/commands/farm.mp4" controls width="600">Your browser does not support the video tag.</video>

```
#farm
```

This will automatically harvest and replant nearby crops. You can specify a range:

```
#farm 20
```

### Tunnel Creation

<video src="/images/baritone/commands/tunnel.mp4" controls width="600">Your browser does not support the video tag.</video>

```
#tunnel
```

Creates a 1x2 tunnel in the direction you're facing.

```
#tunnel 3 2 100
```

Creates a tunnel 3 blocks high, 2 blocks wide, and 100 blocks long.

### World Exploration

```
#explore x z
```

Systematically explores the world from the origin point of x,z.

### Utility Commands

```
#stop
```

Immediately stops all Baritone actions.

```
#click
```

Click destination on screen - right click to path on top of the block, left click to path into it.

### Building Commands

#### Build a Schematic

```
#build schematic_name.schematic
```

Loads and builds the specified schematic from your `schematics` folder.

```
#build example.schematic x y z
```

Builds the schematic with its origin at the specified coordinates.

### Waypoint Commands

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

## Important Settings

Baritone has many settings you can adjust. To toggle a setting, simply type its name in chat.

### Essential Settings

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

### Advanced Settings

```
legitMine
```
Makes mining look more "legitimate" by only mining blocks you can see.

```
followRadius
```
Sets how close Baritone will stay to the entity it's following.

```
mineScanDroppedItems
```
Determines if Baritone will target dropped items while mining.

## Troubleshooting

### Baritone Isn't Responding to Commands

- Make sure Baritone is properly installed
- Check that you're using the correct prefix (default: `#`)

### Baritone Gets Stuck Frequently

- Try adjusting the pathfinding settings
- Ensure you're not in a very complex terrain that's difficult to navigate
- Use `#cancel` and try a different approach or starting point

### Poor Performance

- Reduce render settings for Baritone
- Use simpler goals or shorter paths
- Consider upgrading your computer's RAM allocation to Minecraft

## Additional Resources

- [Official Baritone GitHub](https://github.com/cabaletta/baritone)
- [Baritone Discord Server](http://discord.gg/s6fRBAUpmr)
- [In-depth usage guide](https://github.com/cabaletta/baritone/blob/1.19.4/USAGE.md)