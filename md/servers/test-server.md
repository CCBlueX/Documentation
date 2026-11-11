## CCBlueX's Anti-Cheat Test Server

The CCBlueX test server is a Minecraft server in Europe where you can try LiquidBounce against many different anti-cheats. Add **`test.ccbluex.net`** to your multiplayer server list.

![LiquidBounce on the test server](/images/test-server/world.png)

### Connecting with or without a Minecraft account

You can join without a Minecraft account. The server then puts you in a sign-in lobby, where you sign in with your **LiquidBounce account**. Your name on the server comes from that account and starts with a star (`*`).

| Address | What happens |
|---|---|
| `test.ccbluex.net` | Detects whether your Minecraft session is online or offline. Offline sessions go to the sign-in lobby. If you joined with a premium Minecraft account and want to use your LiquidBounce account, type `/sign-in`. |
| `test-offline.ccbluex.net` | Treats every connection as offline and sends it through LiquidBounce account sign-in. |

After joining, use **`/server latest`** for the 1.21.11 server or **`/server legacy`** for the 1.8.8 server. Both servers share one chat. Each message starts with the server the sender is on, and on Minecraft 1.21.9 and newer you also see the sender's head.

### Selecting anti-cheats

Type **`/ac`** (or `/anticheat`) to open the anti-cheat menu, then click an anti-cheat to pick it. You can also type its name, like `/ac GrimAC`. To pick two, put a space between the names: `/ac GrimAC Vulcan`. Regular players can pick up to two at once. Press Tab while typing to see the names. The menu also shows each anti-cheat's version, author and description if it has them. The two servers don't have the same anti-cheats, and some combinations only work on one of them.

![Anti-cheat selection menu](/images/test-server/anticheats.png)

### Anti-cheats available

**Latest** is the 1.21.11 server (`/server latest`) and **Legacy** is the 1.8.8 server (`/server legacy`). The Server column shows where you can pick each anti-cheat. Open `/ac` after joining to see which ones are turned on right now.

| Anti-cheat | Server | Author(s) | Description |
|---|---|---|---|
| [Intave](https://intave.ac/) | Latest, Legacy | DarkAndBlue, Jpx3, vento, vxcus, lennoxlotl, NotLucky, Trattue | Automated cheat detection and prevention. |
| [GrimAC](https://github.com/GrimAnticheat/Grim) | Latest, Legacy | GrimAC | Simulation based movement checks. |
| [Matrix](https://matrix.rip/) | Latest, Legacy | RE, MIYU | |
| [NoCheatPlus](https://dev.bukkit.org/projects/nocheatplus) | Legacy | NeatMonster and contributors | Checks Minecraft exploits and invalid behavior. |
| [OldNoCheatPlus](https://dev.bukkit.org/projects/nocheatplus) | Legacy | NeatMonster and contributors | Older NoCheatPlus build. |
| [Spartan](https://spartan.top/) | Latest, Legacy | Evangelos Dedes (Vagdedes), pawsashatoy | |
| [AAC5](https://www.spigotmc.org/resources/6442/) | Legacy | konsolas | |
| AGC | Legacy | | |
| AIAC3 | Latest, Legacy | huzpsb | |
| [AntiCheatAddition](https://github.com/Photon-GitHub/AntiCheatAddition) | Latest, Legacy | Photon | Extra checks for cheats other anti-cheats may miss. |
| Axiom | Legacy | dw1e | Private anti-cheat. |
| CoffeeProtect | Legacy | Nik | |
| FairFight | Legacy | dw1e | Lightweight anti-cheat for 1.8 arenas. |
| Frequency | Legacy | Elevated, Gson | |
| Gurei | Latest, Legacy | Gurei | Machine learning anti-cheat. |
| [Hawk](https://github.com/HawkAnticheat/Hawk) | Legacy | Islandscout | |
| [Horizon](https://www.spigotmc.org/resources/65830/) | Legacy | MrCraftGoo, Anthony M., Cipher and other contributors | |
| MX | Latest, Legacy | pawsashatoy, Vagdedes and other contributors | Combat and automation analysis. |
| [Reflex](https://g.reflex.rip/spigot) | Legacy | DarksideCode, sinnlosername | |
| [TakaAntiCheat](https://www.spigotmc.org/resources/45167/) | Legacy | dani02 | |
| Themis | Latest | Olexorus | |
| [TotemGuard](https://github.com/Bram1903/TotemGuard) | Latest | Bram, OutDev | Detects AutoTotem. |
| Verus | Legacy | | |
| [Vulcan](https://vulcanac.net/wiki) | Latest, Legacy | frep, GladUrBad, Joshb_, Elevated, retrooper | |

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
| `/scale [0.5-1.5]` | Changes your player size on the latest server. Without a value it goes back to `1`. |
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
| `/msg <player> <message>`; `/reply <message>` | Sends a private message to a player on any of the servers, or replies to one. |
| `/discord` | Shows the server's Discord link. |
| `/help [page]` | Shows the commands available to you on that server. |
| `/botduel <kit> [easy\|normal\|hard]` | On the practice server, duels a bot with a practice kit. The **Play against a bot** item does the same. |

![Items menu](/images/test-server/items.png)

All commands on this page that start with `/` are **server commands**, not LiquidBounce commands.

### Test bots

The bots around spawn look like real players to your client and to every anti-cheat. Standing and walking bots never die and never get knocked back, so you can hit them as often as you like to test reach, aim and hitboxes. Some show your reach above the hotbar or tell you how much damage you did. Others hit back with a knockback stick so you can test Velocity. Fighter bots attack you with crits, sprint resets and strafing.

### Bot duels

On the practice server, type **`/botduel <kit>`** or use the **Play against a bot** item in the practice lobby to fight a bot that has the same kit as you. **Pick a player** is for duels against real players.

Kits: sword, axe, mace, spear, crystal, elytra, diamond_smp, sumo, boxing, pot, soup, classic, uhc, vanilla, spear_mace and cart. Difficulties: easy, normal and hard. The mace bot launches itself with wind charges and smashes down on you, the diamond SMP bot traps you in cobwebs and walls you off, and the axe bot breaks your shield. Type `/leave` to give up.

The **No Cooldown** switch in the practice menus turns the sword, pot, soup, classic, uhc, sumo and boxing kits into 1.8-style kits without the attack cooldown. It works for queues, duels against players and bot duels. Against a bot you can also type `/botduel <kit>_nocd`, for example `/botduel sword_nocd`.

There are also five minigame kits. You can play them in queues, against players and against bots:

- **floor_is_lava**: the arena fills with lava one layer every 15 seconds, so build up.
- **pillar_of_fortune**: you stand on bedrock pillars over the void and get a random item every 5 seconds.
- **spleef**: dig the snow out from under your opponent.
- **tnt_run**: the floor falls away under your feet.
- **tnt_tag**: hit someone to pass on the TNT before it explodes after 30 seconds.

After a duel, `/duelrematch` challenges the same opponent again, and `/duelrequeue` turns automatic requeueing on or off.
