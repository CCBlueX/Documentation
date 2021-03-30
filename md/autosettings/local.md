## Local AutoSettings
In addition to the possibility to [load configurations](docs/AutoSettings/Overview) from our official repository, it is also possible to create your own and save them locally for later use. To make this possible, LiquidBounce supports a feature called LocalAutoSettings, which allows you to save your current configuration in a file which you can reload at any time or [share](docs/AutoSettings/Uploading%20Settings) with the rest of the community.

The command that makes all this possible is `.localautosettings`. Just like the command for regular AutoSettings, it also has various sub-commands, which are explained in the following.

### How to save your current configuration
With the command `.localautosettings save <name>` you can save your current configuration in a file with the specified name. This file will be saved locally on your hard disk in the LiquidBounce folder. If you are using LiquidBounce 1.8.9 and have not changed the default installation path, it should be located in `%appdata%/.minecraft/LiquidBounce-1.8/settings` under Windows.<br>
If you want to share your configuration with a particular person, you can send him the created file, which he can then store in his settings folder and load with the load sub-command explained below.

![LocalAutoSettings Save]($images$/localsettings_save.png)

### How to load an existing configuration
To restore a configuration you or someone else has previously saved, make sure that the corresponding file is located in the settings folder. If it is, you can reapply it with the load sub-command. The syntax is as follows: `.localautosettings load <name>`. You replace `<name>` with the name of the configuration file you want to load. <br>
An application example would look like this: `.localautosettings load my_server_config.`

![LocalAutoSettings Load]($images$/localsettings_load.png)