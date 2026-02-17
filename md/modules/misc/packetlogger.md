## PacketLogger

Prints all packets and their fields.

**Category:** Misc  
**Enabled by default:** No  

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Filter (Choice | default: BLACKLIST | options: Whitelist, Blacklist)
├── C2SPackets (Registry List)
├── S2CPackets (Registry List)
├── ShowFieldType (Toggle | default: true)
└── OutputTarget (Multi-Select | default: [Chat] | options: Chat, File)
```

### Settings Details

- **Filter** (Choice) — default: `BLACKLIST`; options: `Whitelist`, `Blacklist`
- **C2SPackets** (Registry List)
- **S2CPackets** (Registry List)
- **ShowFieldType** (Toggle) — default: `true`
- **OutputTarget** (Multi-Select) — default: `Chat`; options: `Chat`, `File`

### Screenshots

*Screenshots for PacketLogger will be added in a future update.*

---
*Last updated: 2026-02-13 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/dfe60ac/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fmisc%2FModulePacketLogger.kt)*
