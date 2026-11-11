## PacketLogger

PacketLogger is a tool for developers. It shows every packet (piece of data) that the game and the server send each other, with everything inside it. You can print them in chat, save them to a file in the `packet-logger` folder, or both.

The two packet lists choose which packets you see. With Blacklist, you see everything except the listed packets. With Whitelist, you see only the listed ones.

**Category:** Misc
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Filter | Choice | Blacklist | Whitelist, Blacklist | Whitelist shows only listed packets. Blacklist shows everything except listed packets. |
| C2SPackets | Registry List | | | Packets your game sends to the server. |
| S2CPackets | Registry List | | | Packets the server sends to your game. |
| ShowFieldType | Toggle | true | | Also shows the type of each value. |
| OutputTarget | Multi-Select | Chat | Chat, File | Where the packets go. File saves a new file each time you turn the module on. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/misc/ModulePacketLogger.kt)*
