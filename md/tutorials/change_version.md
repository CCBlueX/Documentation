# How to Change Your Minecraft Version in LiquidBounce

Sometimes, you might need to change your protocol version in LiquidBounce to ensure compatibility with the server you're trying to join.

- **Incompatible client message:** If the server says your client is **NOT** compatible:  
  ![Incompatible Client](/images/incompatible_client.png)

- **AutoConfig suggests using a different version:** If AutoConfig shows your protocol version is **NOT** matching:  
  ![Incompatible Config](/images/incompatible_config.png)

---

### Situation 1: Server has ViaVersion Installed

- **What to Do:** Use the newest Minecraft version when connecting.  
  - With the newest version, the server can recognize you're on a modern client and adjust anti-cheat checks accordingly.  
    This will improve compatibility with their anti-cheat and reduce false flags, or even allow for bypasses.

---

### Situation 2: Server has **NO** ViaVersion Installed

- **What to Do:** Use the Version Selector in LiquidBounce.  
  - You'll find it in the **top-right corner of the Multiplayer menu**.  
  - Select the version required by the server, and ViaFabricPlus will adapt to mimic that version.  
    > Note: This is not a perfect version replication but works for most cases.  

- **Technical Info:** This feature uses **[ViaFabricPlus](https://modrinth.com/mod/viafabricplus)**, a Fabric mod that enables connecting to almost any Minecraft server version. It includes numerous gameplay fixes for compatibility, such as movement, block/entity collisions, and rendering adjustments. ViaFabricPlus supports:  
  - **Release:** 1.0.0 - 1.21.3  
  - **Beta:** b1.0 - b1.8.1  
  - **Alpha:** a1.0.15 - a1.2.6  
  - **Classic:** c0.0.15 - c0.30 (including CPE)  
  - **Bedrock:** 1.21.30 (limited feature support)  
  - **Special Versions:** Snapshots, April Fools, and Combat Tests.  

  > *Disclaimer:* This mod is not guaranteed to work with anti-cheat systems on all servers. Use with caution.

![Version Selector](/images/version_selector.png)

### Situation 3: AutoConfig Suggests Using a Different Version

- **What to Do:** Follow the same steps as in **Situation 2**.  
  - Use the **Version Selector** in the top-right corner of the Multiplayer menu.  

---

By following these steps, you can adjust your protocol version and join any server!