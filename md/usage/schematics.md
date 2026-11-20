## Building Schematics

[AutoBuild](/docs/modules/world/autobuild) can build a whole schematic for you in survival, for example a farm or a house. You load the schematic with the Litematica mod and put it where you want it. AutoBuild then walks around and places every block for you.

AutoBuild only builds schematics that Litematica shows. Without Litematica, the Schematic mode tells you so in chat and turns off.

### What you need

- The Litematica mod and the MaLiLib mod for your Minecraft version. Litematica does not start without MaLiLib.
- A schematic file. Litematica schematics end in `.litematic`.
- All the blocks and items the schematic needs, in your inventory or in chests close by.
- A few spare blocks to stand on, such as dirt or cobblestone. AutoBuild builds small pillars to reach high blocks and takes them away at the end.
- Buckets of water or lava if the schematic has water or lava in it.

### 1. Install Litematica

With LiquidLauncher:

1. Click the cog next to your account to open the settings, then open *Client*.
2. In the list of recommended mods, turn on **Litematica** and **MaLiLib**.
3. Start LiquidBounce.

If your Minecraft version has no Litematica in that list, download both mods from Modrinth ([Litematica](https://modrinth.com/mod/litematica), [MaLiLib](https://modrinth.com/mod/malilib)) and add them with *Add file*. Pick the files made for the Minecraft version you play. See [Using LiquidLauncher](/docs/get-started/liquidlauncher) for more about mods in the launcher.

With another launcher, put both files into the *mods* folder next to LiquidBounce.

To check that it works, join a world and press **M**. The Litematica menu opens.

### 2. Put the schematic into the schematics folder

Litematica reads schematics from the `schematics` folder in your game folder. If the folder is not there, create it and put your `.litematic` file inside.

- LiquidLauncher (Windows): `%APPDATA%/CCBlueX/LiquidLauncher/gameDir/nextgen/schematics`
- LiquidLauncher (Linux): `~/.local/share/liquidlauncher/gameDir/nextgen/schematics`
- LiquidLauncher (macOS): `~/Library/Application Support/liquidlauncher/gameDir/nextgen/schematics`
- Minecraft Launcher: `.minecraft/schematics`

### 3. Load the schematic and place it

1. Stand where the schematic should be built. Litematica puts it at your feet.
2. Press **M** and click **Load Schematics**.
3. Click your schematic in the list.
4. Leave **Create a placement** ticked and click **Load Schematic**.

You now see the schematic as a see-through preview in the world. This preview is called a placement.

To move or turn it, press **M**, click **Schematic Placements** and then **Configure** next to it:

- **Move to player** moves it to where you stand.
- **Rotation** turns it and **Mirror** flips it.
- You can also type the position of its corner by hand.

AutoBuild builds every placement that is switched on. If you have more than one and only want some of them built, click **Placement** in the **Schematic Placements** list to switch the others off.

### 4. Turn on AutoBuild

1. Press **Right Shift** to open the [ClickGUI](/docs/usage/clickgui).
2. Find **AutoBuild** in the **World** panel and right-click it to open its settings.
3. Set **Mode** to **Schematic**.
4. Left-click **AutoBuild** to turn it on.

Stay close to the schematic when you turn it on. AutoBuild only sees placements in the part of the world that is loaded around you.

### While it builds

AutoBuild builds from the bottom up and starts with the blocks closest to you. It places every block facing the right way and sets things like repeaters and comparators the way the schematic has them. Water and lava come from your buckets. Signs stay empty.

- Blocks that are already right stay as they are. To also break blocks that are wrong, turn on **BreakWrongBlocks** in AutoBuild's settings.
- When it runs out of a block, it takes more from chests near you (up to two chunks away) that are not part of the schematic.
- It only places blocks. Item frames, armor stands and other entities are not built.

AutoBuild turns itself off when it is done. You can turn it off at any time to stop it. When you turn it on again, it carries on with what is still missing.

### Chat messages

| Message | What it means | What to do |
|---|---|---|
| Schematic mode needs the Litematica mod | Litematica is not installed. | Install it, see step 1. |
| No enabled Litematica placement nearby | There is no placement, it is switched off, or it is too far away. | Load and place a schematic (step 3) and stand close to it. |
| Built the placement. | Everything is built. | |
| ... blocks left unbuilt. | Some blocks could not be placed. | Read the next messages, fix what they say and turn AutoBuild on again. |
| Missing: ... | These items were not in your inventory or the chests. | Bring them or put them in a chest close by, then turn AutoBuild on again. |
| Carry a spare block to stand on ... | It needed a block to stand on to reach a spot. | Put some dirt or cobblestone in your inventory and turn AutoBuild on again. |

When it is done, look over big redstone builds. Litematica's **Schematic Verifier** (in **Configure**) shows blocks that are missing or wrong.
