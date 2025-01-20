## Auto Config
With the help of Auto Config you can save a specific configuration and reload it later without having to manually adjust all settings again (see [Local Config](docs/AutoConfig/Local%20Config) for how to save configurations). For example, if you have spent time configuring each module to bypass on a particular server, you can simply save the current configuration so that you can easily reload it the next time you play on the server. 

There are two different types of configurations: those that you have saved locally on your hard disk and those that you can load from our public [repository](https://github.com/CCBlueX/LiquidCloud/tree/main/LiquidBounce/settings/nextgen) containing settings for many large servers. You can also upload locally saved configurations you created to the aforementioned repository to share them with the community.

### Auto Config Module
The Auto Config Module, when enabled, will automatically load the config when joining a server. This only works when the server has a known config. Note that while we may provide a config that targets the anti-cheat of the system, the module might not know what anti-cheat the server you joined has.

![Auto Config Module](/images/autoconfig-module.png)

### How to load configurations
As mentioned above, there is an official repository where configurations for a variety of large and small servers are made available for free to the entire community. To access the configurations stored there, the client has special commands. How you can use them, you will find out here.<br>
The commands to manage configurations are explained below.

#### .config list 
When you execute this command, you will obtain a list of available configurations, which you can subsequently load using their respective names.

![Config List](/images/config-list.png)

#### .config load <name>
With this command you can now actually load and apply a pre-made configuration. `<name>` is a placeholder for the name of an available configuration that you know exists based on the previous command.

![Config Load](/images/config-load.png)

#### .config browse
This command opens our GitHub repository (https://github.com/CCBlueX/LiquidCloud/tree/main/LiquidBounce/settings/nextgen) where you can browse configurations and upload your own to share them with the community.