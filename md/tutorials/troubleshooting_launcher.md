## Troubleshooting LiquidLauncher

Use the following guide to troubleshoot common issues with LiquidLauncher. Only contact us through [email](mailto:support@liquidbounce.net) or on our [Discord](/discord) after you verified that all the poissble solutions listed here didn't solve your problem.

### LiquidBounce download does not finish (SmartScreen issue)

This is a known bug on Windows 10. We are currently working on a proper fix. For now, please disable Windows Smart Screen to solve the issue. You can do so by following these steps:

1. Open the start menu and search for *Windows Security*.
2. Open the program and select *App & browser control*.
3. Click *Reputation based protection settings*.
4. Uncheck *Check apps and files* and *SmartScreen for Microsoft Edge*.
5. Restart your computer and try again.

### Fixing issues with the system's hosts file

Some alternative Minecraft authentication services like [EasyMC](https://easymc.io/) and [TheAltening](https://thealtening.com/) may make changes to your system's [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)). These can cause error messages like the following:

- "The authentication servers are down for maintenance."
- "The authentication servers are currently not reachable."
- "Please switch to Mojang mode."
- "Not authenticated with minecraft.net."
- It may also prevent LiquidLauncher from working properly ("An error with the client occured: Connection to https://launchermeta.mojang.com/ failed.").

To reset your hosts file and fix these issues, follow the these instructions for your respective operating system.

#### On Windows
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

#### On macOS and Linux

1. Open a terminal.
2. Execute `sudo nano /etc/hosts`.
3. Enter your computer's password when prompted.
4. Move the cursor using the arrow keys and delete all lines containing either *mojang* or *minecraft*.
5. Press *Ctrl + O* to save and *Ctrl + X* to exit.
6. Restart your computer.

The problems should now be resolved.

#### References
These instructions are based on the ones provided by [sparkuniverse.notion.site](https://sparkuniverse.notion.site/Reverse-changes-by-pirated-versions-2348b6082efa4a0cb59173e965bb5616).

<hr>

### Fixing issues with the DNS server

DNS servers resolve domain names to their corresponding IP address. A misconfigured DNS server can lead to connection issues. We recommend using 1.1.1.1, a DNS server provided by Cloudflare. To set a DNS server, please follow these instructions:

#### On Windows 11

1. Go to *Settings*.
2. Select *Network & internet*
3. Select Wi-Fi or Ethernet depending on your connection.
4. If you selected Wi-Fi in the previous step, click *Properties of [your wifi's name]*.
5. Under DNS server assignment, select *Edit*.
6. From the drop-down menu, select *Manual*.
7. Turn on the IPv4 toggle switch.
8. Under Preferred DNS, enter `1.1.1.1` and `1.0.0.1`.
9. Hit *Save* and restart your computer.

#### On Windows 10, 8 & 7

1. Open the control panel.
2. Select *Network and Sharing Center*.
3. Click *Change adapter settings* on the left side of the window.
4. Double click your current internet connection whether it’s Wi-Fi or Ethernet.
5. Click *Properties* in the window that popped up.
6. Select *Internet Protocol Version 4 (TCP/IPv4)* from the list under *This connection uses the following items*.
7. Press *Properties*.
8. Change the radio button to *Use the following DNS server addresses*.
9. Enter `1.1.1.1` as preferred DNS and `1.0.0.1` as alternate DNS.
10. Press *OK* and restart your computer

####  On macOS

Please follow [this guide](https://support.apple.com/guide/mac-help/change-dns-settings-on-mac-mh14127/mac) provided by Apple.

#### On Linux

DNS configuration varies depending on your distribution and desktop environment. Please lookup a matching guide yourself. Since you are a Linux user, you probably know how to use a search engine.
