## PacketLogger

PacketLogger captures every network packet exchanged between your client and the server and prints its contents — the packet class name, protocol ID, direction (incoming or outgoing), and the value of every field inside the packet. This makes it a powerful diagnostic tool for understanding exactly what data is being sent and received at any given moment, whether you are investigating server behaviour, debugging other modules, or exploring how specific actions translate into network traffic.

You can narrow what gets logged by combining the **Filter** mode with the **C2SPackets** and **S2CPackets** registry lists. In **Whitelist** mode only the packets you add to those lists are shown; in **Blacklist** mode everything is logged *except* the packets you list, which is useful for hiding high-frequency noise (e.g. position packets) while keeping everything else visible. Output can go to in-game **Chat**, to a **CSV file** saved in the `packet-logger` folder inside LiquidBounce's config directory, or to both at the same time. The file is created fresh each time the module is enabled and named after the current date and time.

Note that PacketLogger is intentionally excluded from auto-config profiles — it is a debugging utility and is not meant to be saved into your normal gameplay presets.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Filter | Choice | Whitelist | Whitelist, Blacklist | Determines whether the packet lists below act as a whitelist (log only listed packets) or a blacklist (log everything except listed packets). |
| C2SPackets | Registry List | — | — | List of client-to-server (outgoing) packet types to include or exclude, depending on the Filter mode. |
| S2CPackets | Registry List | — | — | List of server-to-client (incoming) packet types to include or exclude, depending on the Filter mode. |
| ShowFieldType | Toggle | true | — | When enabled, each logged field is annotated with its Java type (e.g. `int`, `BlockPos`) alongside its name and value. |
| OutputTarget | Multi-Select | Chat | Chat, File | Where packet output is sent. Select **Chat** to see packets in the in-game chat, **File** to write a timestamped CSV log, or both simultaneously. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModulePacketLogger.kt)*
