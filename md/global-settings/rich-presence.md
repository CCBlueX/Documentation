## RichPresence

Shows on your Discord profile that you are playing LiquidBounce, with the details you pick. Discord has to be open on the same computer. If the client cannot find Discord, it shows a message and stops trying until you turn this off and on again.

**Aliases:** DiscordPresence  
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Enabled | Toggle | On | | Shows LiquidBounce on your Discord profile. |
| ActivityType | Choice | Competing | Playing, Listening, Watching, Competing | The word Discord puts before the name, like "Playing" or "Competing in". |
| StatusDisplayType | Choice | Name | Name, State, Details | Which text Discord shows next to your name in the member list. |
| Separator | Text | ` - ` | | Text put between two parts. |
| DetailsParts | Multi-Select | ClientName, ClientVersion | see the parts below | What the first line shows. |
| StateParts | Multi-Select | Modules, ClientCommit | see the parts below | What the second line shows. |
| LargeImage | Toggleable Group | On | | Shows the big picture. |
| LargeImage → Asset | Choice | Logo | Logo | The picture. |
| LargeImage → Parts | Multi-Select | ProtocolVersion | see the parts below | Text shown when someone hovers over the big picture. |
| SmallImage | Toggleable Group | Off | | Shows the small picture in the corner of the big one. |
| SmallImage → Asset | Choice | Logo | Logo | The picture. |
| SmallImage → Parts | Multi-Select | ClientBranch, ClientCommit | see the parts below | Text shown when someone hovers over the small picture. |

### Parts

| Part | Shows |
|---|---|
| ClientName | LiquidBounce |
| ClientVersion | The client version |
| ClientAuthor | CCBlueX |
| ClientBranch | The branch the client was built from |
| ClientCommit | The commit the client was built from |
| Modules | How many modules are on out of all modules |
| MinecraftVersion | The Minecraft version you play |
| ProtocolVersion | The Minecraft version you joined the server with |
| Server | The server you are on. Addresses that should stay private are hidden. |

Your profile also gets two buttons: Website (liquidbounce.net) and LiquidProxy (liquidproxy.net).

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/global/GlobalSettingsRichPresence.kt)*
