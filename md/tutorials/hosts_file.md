## How to fix a proken hosts file

Some alternative Minecraft authentication services like [EasyMC](https://easymc.io/) and [TheAltening](https://thealtening.com/) may make changes to your system's [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)). These can cause error messages like the following:

- "The authentication servers are down for maintenance."
- "The authentication servers are currently not reachable."
- "Please switch to Mojang mode."
- "Not authenticated with minecraft.net."
- It may also prevent LiquidLauncher from working properly.

To reset your hosts file and fix these issues, follow the following instructions.

### On Windows
1. Search for *notepad* in start menu, right-click it, and run it as an administrator. <br>
![versions](/images/hosts_file/step_1.png)

2. Click *Yes* to allow the program to make changes to your device. <br>
![versions](/images/hosts_file/step_2.png)

3. In the Notepad window, click *File* and then select *Open...*. <br>
![versions](/images/hosts_file/step_3.png)

4. Navigate to *C:\\Windows\\System32\\drivers\\etc\\*.
5. Select *All Files* from the drop down in the bottom right corner of the window.
6. Open the file called *hosts*. <br>
![versions](/images/hosts_file/step_4.png)

7. Remove all lines containing either *mojang* or *minecraft*. <br>
![versions](/images/hosts_file/step_5.png)

8. Save the file and restart your computer.

The problems should now be resolved.

### On macOS and Linux

1. Open a terminal.
2. Execute `sudo nano /etc/hosts`.
3. Enter your computer's password when prompted.
4. Move the cursor using the arrow keys and delete all lines containing either *mojang* or *minecraft*.
5. Press *Ctrl + O* to save and *Ctrl + X* to exit.
6. Restart your computer.

The problems should now be resolved.

#### References
These instructions are based on the ones provided by [sparkuniverse.notion.site](https://sparkuniverse.notion.site/Reverse-changes-by-pirated-versions-2348b6082efa4a0cb59173e965bb5616).