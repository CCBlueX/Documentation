## AutoSettings
With the help of AutoSettings you can save a specific configuration and reload it later without having to manually adjust all settings again. For example, if you have spent time configuring each module to bypass on a particular server, you can simply save the current configuration so that you can easily reload it the next time you play on the server. 

There are two different types of AutoSettings: those that you have saved locally on your hard disk and those that you can load from our public [repository](https://github.com/CCBlueX/LiquidCloud/tree/master/LiquidBounce/settings) containing settings for many large servers. You can also upload locally saved AutoSettings you created to the aforementioned repository to share them with the community. To learn more about this, click [here](docs/AutoSettings/Uploading%20Settings).

### How to load settings from the official repository
As mentioned above, there is an official repository where AutoSettings for a variety of large and small servers are made available for free to the entire community. To access the configurations stored there, the client has a special command. How you can use it, you will find out here.<br>
The command to load settings from our repository is called `.autosettings`. As a little reminder, you can execute client commands by typing them in the chat. 

The AutoSettings command has two sub-commands, which are explained below.

#### .autosettings list
When you execute this command, you will obtain a list of available configurations, which you can subsequently load using their respective names.

![AutoSettings List](/images/autosettings_list.png)

#### .autosettings load <name>
With this command you can now actually load and apply a pre-made configuration. `<name>` is a placeholder for the name of an available configuration that you know exists based on the previous command. <br>
An example of using this command would be `.autosettings load hypixel` to apply the current Hypixel configuration.

![AutoSettings Load](/images/autosettings_load.png)