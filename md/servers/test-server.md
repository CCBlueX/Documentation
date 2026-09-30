## CCBlueX's Anti-Cheat Test Server

The CCBlueX Testserver is an EU Minecraft server for trying LiquidBounce against different anti-cheats. Add **`test.ccbluex.net`** to your multiplayer server list.

![LiquidBounce on the test server](/images/test-server/world.png)

### Connecting with or without a Minecraft account

You can join without a Minecraft account. In that case, sign in with your **LiquidBounce account** when the server puts you in the sign-in lobby. Your server name comes from that account; names signed in this way have a star (`*`) prefix.

| Address | What happens |
|---|---|
| `test.ccbluex.net` | Detects whether your Minecraft session is online or offline. Offline sessions go to the sign-in lobby. If you joined with a premium Minecraft account and want to use your LiquidBounce account, type `/sign-in`. |
| `test-offline.ccbluex.net` | Treats every connection as offline and sends it through LiquidBounce account sign-in. |

After joining, use **`/server latest`** for the 1.21.11 server or **`/server legacy`** for the 1.8.8 server.

### Selecting anti-cheats

Type **`/ac`** (or `/anticheat`) to open the anti-cheat menu. Click an anti-cheat to select it. You can also type `/ac <name>` to select one directly, such as `/ac GrimAC`. To select multiple installed anti-cheats, separate their names with spaces, for example `/ac GrimAC Vulcan`. Regular players can select up to two at once. Tab completion shows available names. The menu shows each plugin's version, author and description when supplied by that plugin. Availability and allowed combinations can differ between the two servers.

![Anti-cheat selection menu](/images/test-server/anticheats.png)

### Anti-cheats available

**Latest** is the 1.21.11 server (`/server latest`); **Legacy** is the 1.8.8 server (`/server legacy`). The server column shows where each anti-cheat is listed. Open `/ac` after joining to see which plugins are currently enabled.

| Anti-cheat | Server | Author(s) | Description |
|---|---|---|---|
| [Intave](https://intave.ac/) | Latest, Legacy | DarkAndBlue, Jpx3, vento, vxcus, lennoxlotl, NotLucky, Trattue | Automated cheat detection and prevention. |
| [GrimAC](https://github.com/GrimAnticheat/Grim) | Latest, Legacy | GrimAC | Simulation based movement checks. |
| [Matrix](https://matrix.rip/) | Latest, Legacy | RE, MIYU | — |
| [NoCheatPlus](https://dev.bukkit.org/projects/nocheatplus) | Legacy | NeatMonster and contributors | Checks Minecraft exploits and invalid behavior. |
| [OldNoCheatPlus](https://dev.bukkit.org/projects/nocheatplus) | Legacy | NeatMonster and contributors | Older NoCheatPlus build. |
| [Spartan](https://spartan.top/) | Latest, Legacy | Evangelos Dedes (Vagdedes), pawsashatoy | — |
| [AAC5](https://www.spigotmc.org/resources/6442/) | Legacy | konsolas | — |
| AGC | Legacy | — | — |
| AIAC3 | Latest, Legacy | huzpsb | — |
| [AntiCheatAddition](https://github.com/Photon-GitHub/AntiCheatAddition) | Latest, Legacy | Photon | Extra checks for cheats other anti-cheats may miss. |
| Axiom | Legacy | dw1e | Private anti-cheat. |
| CoffeeProtect | Legacy | Nik | — |
| FairFight | Legacy | dw1e | Lightweight anti-cheat for 1.8 arenas. |
| Frequency | Legacy | Elevated, Gson | — |
| Gurei | Latest, Legacy | Gurei | Machine learning anti-cheat. |
| [Hawk](https://github.com/HawkAnticheat/Hawk) | Legacy | Islandscout | — |
| [Horizon](https://www.spigotmc.org/resources/65830/) | Legacy | MrCraftGoo, Anthony M., Cipher and other contributors | — |
| MX | Latest, Legacy | pawsashatoy, Vagdedes and other contributors | Combat and automation analysis. |
| [Reflex](https://g.reflex.rip/spigot) | Legacy | DarksideCode, sinnlosername | — |
| Sentinel | Latest, Legacy | — | — |
| [TakaAntiCheat](https://www.spigotmc.org/resources/45167/) | Legacy | dani02 | — |
| Themis | Latest | Olexorus | — |
| [TotemGuard](https://github.com/Bram1903/TotemGuard) | Latest | Bram, OutDev | Detects AutoTotem. |
| Verus | Legacy | — | — |
| [Vulcan](https://vulcanac.net/wiki) | Latest, Legacy | frep, GladUrBad, Joshb_, Elevated, retrooper | — |

### Commands

| Command | What it does |
|---|---|
| `/menu` | Opens the main server menu. |
| `/ac [name ...]` | Opens the anti-cheat menu or selects one or more anti-cheats by name. |
| `/items` or `/i` | Opens the item menu for test gear. |
| `/give <item> [amount]` | Gives yourself an item. Some items are restricted. |
| `/enchant` | Opens the enchantment menu for an item. |
| `/effect <effect> [seconds] [amplifier]` | Applies a potion effect, subject to server restrictions. |
| `/repair` | Repairs repairable items in your inventory and armor slots. |
| `/heal` | Restores health and food. |
| `/health <amount>`; `/hunger <amount>` | Sets your own health or hunger. |
| `/damage [amount]` | Damages you to test reactions to damage and knockback. |
| `/damagetick <0-20>` | Changes your invulnerability ticks after taking damage. |
| `/scale [0.5-1.5]` | Changes your player scale on the latest server; omitting the value resets it to `1`. |
| `/kill` | Kills your character for respawn testing. |
| `/clear` | Empties your inventory. |
| `/filtersystem` or `/fs` | Opens the event and packet filter menu. |
| `/exploit` | Opens the server's exploit test menu. `/exploit list` shows the available tests; execution asks for confirmation. |
| `/warp` or `/warp <name>` | Opens the warp menu or teleports to a named warp. |
| `/spawn`; `/back` | Goes to spawn or returns to your last death location. |
| `/tpa <player>`; `/tpahere <player>` | Requests a teleport to a player or asks them to teleport to you. |
| `/tpaccept`; `/tpdeny`; `/tpacancel` | Responds to or cancels a teleport request. |
| `/settings`; `/language [language]` | Opens server settings or changes your language. |
| `/ping`; `/gameprotocol` | Shows your ping or protocol version. |
| `/client` | Shows client information. |
| `/msg <player> <message>`; `/reply <message>` | Sends a private message or replies to one. |
| `/discord` | Shows the server's Discord link. |
| `/help [page]` | Shows the commands available to you on that server. |

![Items menu](/images/test-server/items.png)

Commands beginning with `/` here are **server commands**.
