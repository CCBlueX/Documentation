# Building with Baritone

## Building Schematics

### Prerequisites
1. Place your schematic files in the `schematics` folder of your Minecraft directory
2. Ensure you have the required building materials in your inventory
3. Have appropriate tools ready for breaking blocks if needed

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
1. When you start the build, Baritone will analyze the schematic and list required materials
2. If materials are missing, Baritone will display "missing material" messages in chat
3. Place required materials in your hotbar
4. Baritone will automatically place blocks according to the schematic
5. Keep appropriate tools in your inventory as Baritone may need to break blocks during construction

## Build Settings
- Use `allowPlace` to enable/disable block placement
- Adjust `buildIgnoreBlocks` for specific block exclusions
- Use `buildRepeatTimeout` to control rebuild attempts
