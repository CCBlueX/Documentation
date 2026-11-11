# Building with Baritone

## Building Schematics

### Prerequisites
1. Place your schematic files in the `schematics` folder of your Minecraft directory
2. Have the building blocks you need in your inventory
3. Bring tools in case blocks need to be broken

### Build Command
```
#build schematic_name.schematic
```

Loads and builds the specified schematic from your `schematics` folder.

```
#build example.schematic x y z
```

Builds the schematic with its origin at the specified coordinates.

### Building Process
1. When you start the build, Baritone reads the schematic and lists the blocks it needs
2. If blocks are missing, it says so in chat
3. Put the needed blocks in your hotbar
4. Baritone places the blocks for you
5. Keep tools in your inventory, since Baritone may need to break blocks while building

## Build Settings
- `allowPlace` turns block placing on or off
- `buildIgnoreBlocks` lists blocks the builder should skip
- `buildRepeatTimeout` controls how long Baritone waits before trying to build again
