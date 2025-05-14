# How to use Baritone

Baritone uses a command prefix system to distinguish its commands from regular chat. The default prefix is `#`, so all Baritone commands will start with this symbol (e.g., `#goal`, `#mine`, etc.).

> **Note:** You can use commands directly in chat. Be careful with typos, as they will be sent to public chat if you make mistakes.

## Usage Documentation

Learn more about specific Baritone features:

- [Movement & Pathfinding](movement.md) - Navigation and path control
- [Mining](mining.md) - Automated mining
- [Farming & Resource Gathering](farming.md) - Automated farming
- [Combat & PvP](fighting.md) - Automated combat
- [Building & Construction](building.md) - Schematic building and construction
- [Settings & Configuration](settings.md) - Customizing Baritone behavior

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

### Basic Navigation

```
#stop
```
Immediately stops all Baritone actions.

```
#click
```
Click destination on screen - right click to path on top of the block, left click to path into it.

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
