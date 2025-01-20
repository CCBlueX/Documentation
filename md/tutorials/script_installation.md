## Scripts
LiquidBounce provides an interface that allows third-party developers from our community to enhance the client with new features using JavaScript scripts. These scripts can add various functionalities - from simple [macros](https://forum.liquidbounce.net/topic/8354/script-macros) to complex features like an [NES Emulator](https://forum.liquidbounce.net/topic/8352/script-nes-emulator).

### Managing Scripts
The following commands are available to manage your scripts:

#### .script list
Shows a list of all installed scripts.

![Script List](/images/script-list.png)

#### .script browse
Opens the scripts folder where all your scripts are stored. This is the easiest way to access the scripts directory.

#### .script load <name>
Loads a specific script. Replace `<name>` with the script's filename.

#### .script unload <name>
Unloads a specific script. Replace `<name>` with the script's filename.

#### .script reload
Reloads all scripts. Use this command after adding new scripts to load them into the client.

#### .script edit <name>
Opens a script in your default text editor for modifications.

#### .script debug <name> [protocol] [suspend on start] [inspect internals] [port]
Enables DevTools debugging for a specific script. Additional parameters can be configured for debugging purposes.

### Installing Scripts
You can find scripts in our [community forum's script section](https://forum.liquidbounce.net/category/25/scripts). To install a script:

1. Type `.script browse` to open the scripts folder
2. Copy the script file into this folder (if it's a zip file, extract it first)
3. Type `.script reload` to load the new script
4. Use `.script list` to verify the script was loaded successfully

![Script Directory](/images/script-directory.png)

### Developing Scripts
LiquidBounce's script API is based on GraalJS, an ECMAScript 2023 compliant JavaScript implementation built on GraalVM. This allows scripts to seamlessly interact with the client's Java and Kotlin codebase, making it particularly intuitive for those familiar with Minecraft modding.

If you're interested in developing your own scripts, please refer to our [Script API documentation](docs/Script%20API/Getting%20Started) for detailed information on how to create and develop scripts.