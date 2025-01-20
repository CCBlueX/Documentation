## Local Config
In addition to the possibility to load configurations from our official repository, it is also possible to create your own and save them locally for later use. To make this possible, LiquidBounce supports a feature called Local Config, which allows you to save your current configuration in a file which you can reload at any time or share with the rest of the community.

The commands that make all this possible are explained in the following sections.

### How to manage your local configurations
The following commands are available for managing your local configurations:

#### .localconfig save <name> [binds]
With this command you can save your current configuration in a file with the specified name. This file will be saved locally on your hard disk in the LiquidBounce configs folder (usually located at %AppData%/liquidlauncher/gameDir/nextgen/LiquidBounce/configs). You can optionally include binds in the saved configuration by adding the 'binds' parameter.<br>
If you want to share your configuration with a particular person, you can send them the created file, which they can then store in their configs folder and load with the load command explained below.

![LocalConfig Save](/images/localconfig-save.png)

#### .localconfig load <name>
To restore a configuration you or someone else has previously saved, make sure that the corresponding file is located in the configs folder. If it is, you can reapply it with the load command. You replace `<name>` with the name of the configuration file you want to load.

![LocalConfig Load](/images/localconfig-load.png)

#### .localconfig browse
This command will open the directory containing your local configurations (usually located at %AppData%/liquidlauncher/gameDir/nextgen/LiquidBounce/configs).

Please note that the Auto Config module will only detect and use online configs from the repository, not local configs.