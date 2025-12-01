# Troubleshooting FPS Drops & Freezing

If you're experiencing frame rate drops or freezing with LiquidBounce, whether while playing or when interacting with the GUI (HUD, ClickGUI, menu), this guide will help you resolve the issue.

## 1. Check RAM Allocation

Insufficient RAM allocation is one of the most common causes of performance issues. Ensure Java has enough memory allocated:

#### Using LiquidLauncher

LiquidLauncher sets the default RAM allocation to 4 GiB, which should be sufficient for most users. However, you can verify and adjust if needed:

1. Open LiquidLauncher
2. Go to **Settings** or **Launch Options**
3. Check the RAM allocation (should be at least 4 GiB)
4. Adjust if necessary

![LiquidLauncher Memory Settings](/images/troubleshooting_fps/liquidlauncher-memory-settings.png)

#### Using Minecraft Launcher

The official Minecraft Launcher often defaults to only 2 GiB, which may not be enough:

1. Open Minecraft Launcher
2. Go to **Installations** tab
3. Click on your installation (hover and click the **three dots** → **Edit**)
4. Click **More Options**
5. Find the **JVM Arguments** field
6. Look for `-Xmx2G` (this means 2 GiB maximum)
7. Change it to `-Xmx4G` (or `-Xmx6G` if you have 16GB+ of system RAM)
8. Also ensure `-Xms` matches, e.g., `-Xms4G -Xmx4G`
9. Save and launch

For more detailed instructions, see this [tutorial on allocating RAM to Minecraft](https://www.minecraftforum.net/forums/support/java-edition-support/3001598-tutorial-how-to-allocate-more-ram-to-minecraft).

#### Check System Environment Variables

Java memory settings can also be configured through system environment variables, which may override launcher settings:

**Windows:**
1. Press `Win + R`, type `sysdm.cpl`, and press Enter
2. Go to **Advanced** tab → **Environment Variables**
3. Check both **User variables** and **System variables** for:
   - `_JAVA_OPTIONS`
   - `JAVA_TOOL_OPTIONS`
   - `JDK_JAVA_OPTIONS`
4. If any of these contain `-Xmx` or `-Xms` parameters with low values (e.g., `-Xmx2G`), either:
   - Remove the variable entirely, or
   - Increase the values to at least `-Xms4G -Xmx4G`
5. Click **OK** and restart your computer

**Linux/macOS:**
1. Check your shell configuration file (`~/.bashrc`, `~/.zshrc`, or `~/.profile`)
2. Look for exports like:
   ```bash
   export _JAVA_OPTIONS="-Xmx2G"
   export JAVA_TOOL_OPTIONS="-Xmx2G"
   ```
3. Either remove these lines or increase the values to `-Xmx4G`
4. Reload your shell: `source ~/.bashrc` (or restart terminal)

**Note:** Recommended allocation is 4-6 GiB. Don't allocate too much (avoid using more than 50% of your total system RAM).

#### Verify RAM Allocation In-Game

You can check if Minecraft is actually using the allocated RAM:

1. Launch Minecraft with LiquidBounce
2. Press **F3** to open the debug screen
3. Look at the top right corner for memory information (e.g., "Mem: 25% 1024/4096MB")
4. The second number should match your allocated RAM (e.g., 4096MB = 4GB)

![F3 Memory Display](/images/troubleshooting_fps/f3-memory.png)

## 2. Check RAM Speed (Critical)

The speed of your RAM is crucial for LiquidBounce's performance. CEF (Chromium Embedded Framework) renders to a bitmap that gets uploaded to the GPU from memory. Slow RAM will cause lag regardless of your GPU performance.

You can benchmark your RAM's performance in relation to CEF rendering using the [gl-bench](https://github.com/1zun4/gl-bench) tool. This will help you identify if RAM speed is your bottleneck.

#### Enable XMP in BIOS

XMP (Extreme Memory Profile) allows your RAM to run at its rated speed instead of the default slower speed:

1. Restart your computer and enter BIOS (usually by pressing `Delete`, `F2`, or `F12` during boot)
2. Find the XMP/DOCP/EOCP setting (location varies by motherboard manufacturer):
   - **ASUS/MSI/Gigabyte:** Usually under "AI Tweaker", "OC", or "Advanced" settings
   - **AMD motherboards:** Look for DOCP (Direct Overclock Profile)
3. Enable XMP Profile 1 (or DOCP)
4. Save and exit BIOS

**This solution has been confirmed to fix FPS drops in many cases.**

![XMP Fix Success](/images/troubleshooting_fps/xmp-fix-success.png)

#### Check RAM Slot Configuration

Ensure your RAM sticks are seated in the fast/optimal slots:

1. Consult your motherboard manual for the recommended RAM slot configuration
2. For dual-channel setups with 2 sticks, typically use slots 2 and 4 (or A2 and B2)
3. Reseat RAM sticks if necessary

#### Alternative: Reset BIOS Settings

If you're not comfortable tweaking BIOS settings, you can try resetting to defaults:

1. Enter BIOS
2. Find "Load Optimized Defaults" or "Reset to Default"
3. Save and exit

## 3. Verify GPU is Being Used

A common cause of poor performance is the monitor being connected to the motherboard instead of the GPU, which causes the system to use integrated graphics instead of your dedicated graphics card.

#### Check Your Monitor Connection

1. Look at the back of your computer
2. Identify where your monitor cable is plugged in:
   - **Correct:** Cable is plugged into your graphics card (usually lower on the case, in a separate expansion slot)
   - **Incorrect:** Cable is plugged into the motherboard (usually higher up, near USB ports and audio jacks)
3. If plugged into the motherboard, shut down your computer and move the cable to your GPU

#### Verify in Windows

1. Open **Task Manager** (`Ctrl + Shift + Esc`)
2. Go to the **Performance** tab
3. Look for **GPU 0** and **GPU 1** (if you have integrated graphics)
4. Launch Minecraft with LiquidBounce
5. Check which GPU shows activity - it should be your dedicated GPU (e.g., NVIDIA/AMD), not Intel integrated graphics

## 4. Update GPU Drivers

Outdated GPU drivers can cause performance issues and compatibility problems:

**NVIDIA:**
1. Visit [NVIDIA Driver Downloads](https://www.nvidia.com/Download/index.aspx)
2. Select your GPU model and operating system
3. Download and install the latest Game Ready Driver

**AMD:**
1. Visit [AMD Driver Downloads](https://www.amd.com/en/support)
2. Select your GPU model
3. Download and install the latest Adrenalin driver

**Intel:**
1. Visit [Intel Driver & Support Assistant](https://www.intel.com/content/www/us/en/support/detect.html)
2. Use the auto-detect tool or manually select your GPU
3. Download and install the latest driver

## 5. Enable Accelerated Rendering (Windows Only)

For Windows users, enabling accelerated rendering can significantly improve performance:

1. Go to **HUD** → **Global Renderer** → **Accelerated (BETA)**
2. Enable it

**Important Notes:**
- **Windows only:** This feature is only supported on Windows systems
- **AMD GPU users:** There is a known [VRAM leak bug](https://github.com/chromiumembedded/cef/issues/3968) that may cause VRAM to fill up after extended use. Monitor your VRAM usage.
- **NVIDIA GPU users:** This option generally works well and is recommended
- **Intel GPU users:** This feature is not currently supported due to [driver issues](https://github.com/IGCIT/Intel-GPU-Community-Issue-Tracker-IGCIT/issues/1143)
- **Experimental:** This feature is still in beta, so report any issues you encounter

## 6. Optimize HUD and Theme Settings

#### Use Default Theme

Custom themes can cause performance issues. Use the default theme:

1. Open the in-game chat
2. Execute the command: `.client theme set liquidbounce`
3. The default theme will be applied immediately

For more information about the theme system, visit: [Theme System Overview](/docs/theme-system/overview)

#### Disable Unnecessary HUD Components

Disabling HUD components you don't use can improve performance:

1. Go to **HUD** → **Components** → **Name of the Theme** (e.g., LiquidBounce)
2. Review all enabled HUD elements
3. Disable components you don't need

For detailed information on HUD customization, visit: [HUD Customization](/docs/theme-system/hud-customization)

## 7. Limit GUI Renderer FPS

The GUI renderer can consume excessive resources if left uncapped. Limiting it to 60 FPS can significantly improve performance:

**For HUD:**
1. Go to **HUD** → **Renderer** → **FPS**
2. Set the FPS limit to `60`

**For ClickGUI:**
1. Go to **ClickGUI** → **Renderer** → **FPS**
2. Set the FPS limit to `60`

## 8. Remove Conflicting Mods

Third-party mods can cause performance issues or conflicts with LiquidBounce:

1. Create a backup of your mods folder
2. Remove all mods except LiquidBounce and it's dependencies
3. Test if the FPS issue persists
4. If the issue is resolved, add mods back one by one to identify the mod causing the issue.

## 9. Reduce Rendering Quality (Last Resort)

If nothing else helps and you're still experiencing severe performance issues, you can reduce the rendering quality. **This will make the GUIs look significantly worse** (rendering at half resolution), but it can drastically improve performance:

1. Go to **HUD** → **Global Renderer** → **Quality**
2. Lower the quality setting

**Warning:** This is a last resort option as it notably degrades visual quality. Only use this if all other solutions have failed.

## Still Having Issues?

If you continue to experience problems after trying all the solutions above, please [contact our support team](https://ccbluex.net/contact) with:

- Your system specifications (CPU, GPU, RAM)
- Minecraft version and LiquidBounce build
- Steps to reproduce the issue
- Your latest.log file from the logs folder:
  - **LiquidLauncher (Windows):** `%APPDATA%/CCBlueX/LiquidLauncher/gameDir/nextgen/logs`
  - **LiquidLauncher (Linux):** `~/.local/share/liquidlauncher/gameDir/nextgen/logs`
  - **LiquidLauncher (macOS):** `~/Library/Application Support/liquidlauncher/gameDir/nextgen/logs`
  - **Minecraft Launcher:** `.minecraft/logs/`
- A video showing the issue (if possible)
