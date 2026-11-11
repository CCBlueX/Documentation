## LiquidProxy

[LiquidProxy](https://liquidproxy.net) is a game proxy for Minecraft Java Edition only. It gives your connection a different IP address, so you can get past IP bans and AntiVPN plugins. It is a separate paid subscription and needs no download.

### Plans

| | Basic | Pro |
|---|---|---|
| Dedicated network | Yes | Yes |
| Residential network | No | Yes |
| Accounts at once | 2 | 2 |

- **Dedicated**: data center IPs. Lowest ping, and a connection can last up to a week. Some AntiVPN plugins detect it.
- **Residential**: home connection IPs. Gets past strict AntiVPN (v4Guard and similar).

#### Which plan do I need?

Enter your server in the **Server Compatibility Checker** on [liquidproxy.net](https://liquidproxy.net/#server-checker), below the plans. It recommends a plan based on our latest test of that server.

![Server Compatibility Checker recommending Pro](/images/liquidproxy-server-checker.png)

- **We recommend Basic** or **We recommend Pro**: this plan got in when we tested the server.
- **Not tested yet**: Pro is the safer pick. You can ask us to test the server.
- **No plan works here right now**: the server blocks all our networks or only lets in certain countries.

Servers change their AntiVPN, so a recommendation is not a guarantee.

Upgrade (you pay only the difference) or cancel under **Manage Subscription** at [liquidproxy.net/subscription](https://liquidproxy.net/subscription).

### Connect

Open the [dashboard](https://liquidproxy.net/dashboard). The **Connect** card has two ways to connect. Video: [setup tutorial](https://www.youtube.com/watch?v=W0dSieDq2qQ).

#### Proxy Manager (recommended)

![Proxy Manager tab of the Connect card](/images/liquidproxy-proxy-manager.png)

1. Pick a **Proxy type**, **Port** and **Location**. **Smart** picks the network that works on each server; **Auto** picks the closest location.
2. Copy the **URL**, e.g. `socks5://user:pass@smart.eu-fra.liquidproxy.net:1080`. Click a part of it to copy only that part.
3. In LiquidBounce open the [Proxy Manager](/docs/usage/proxy-manager), press **Add from Clipboard**, select the proxy and join.

Ports 80, 443, 993, 1080 and 25565 all take HTTP and SOCKS5. If one doesn't connect, try 443. **Regenerate credentials** makes a new password, and the old one stops working right away.

#### Minecraft Routes (any client)

![Minecraft Routes tab of the Connect card](/images/liquidproxy-minecraft-routes.png)

1. **Add route** with the server address.
2. Copy the route into your Minecraft server list and join it.

A route made on **Auto** follows the location picked above, so copy it again after changing location. If a server says "Not authenticated with Minecraft.net", use the Proxy Manager.

### Locations

Frankfurt, Gravelines, London, Stockholm, Warsaw, Madrid, Los Angeles, Chicago, Seattle, New York, Atlanta, Beauharnois, São Paulo, Singapore. Pick the one closest to the game server. The list shows your ping to each one.

### IPs

- Each Minecraft name keeps the same IP per server and location, and no other player gets it there.
- You get a new one after 3 days without joining, when the IP stops working, or when you press **New IP on next join** in **Connections**.

### Dashboard

![Connections card](/images/liquidproxy-connections.png)

**Connections** lists your games of the last 7 days: green is playing now (power button disconnects), yellow is an offline account with a saved IP, white is past. Open a row to see the server and IP type. **Usage** shows your total playtime, servers, accounts and IPs.

### Limits

- 2 Minecraft accounts at once per subscription. If you see "maximum number of simultaneous connections", disconnect somewhere else or wait a few minutes. For more accounts you need another subscription.

### Troubleshooting

| Problem | Fix |
|---|---|
| Frequent disconnects | Try another location, check the network (Dedicated vs. Residential) and your protocol version. |
| Network protocol error | Not LiquidProxy: use the right protocol version, turn off **Auto Config** if it changes it. |
| Server still detects VPN | Use Residential, a location in the server's country, or **New IP on next join**. Try another account if it got restricted. |
| Hypixel "Security blocked" | This comes from low-quality alt accounts. The proxy doesn't cause it. |
| Subscription missing | Log out and in again, check the payment went through. |

Still stuck? [Contact support](https://ccbluex.net/contact) with your UID ([liquidproxy.net/account](https://liquidproxy.net/account)), the server, location and network.
