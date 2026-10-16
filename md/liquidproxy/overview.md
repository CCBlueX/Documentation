## LiquidProxy

[LiquidProxy](https://liquidproxy.net) is a proxy service built specifically for Minecraft. It allows you to change your IP address when connecting to Minecraft servers, which is useful for bypassing IP bans and servers running AntiVPN plugins.

> LiquidProxy is a separate paid service. You can subscribe at [liquidproxy.net](https://liquidproxy.net).

### How LiquidProxy Works

LiquidProxy routes your Minecraft connection through proxy servers so that the game server sees a different IP address instead of your real one. Unlike a traditional VPN, LiquidProxy only affects your Minecraft connection and is optimized to minimize latency.

LiquidProxy operates on a **fair-use** basis and is made for Minecraft Java Edition. It is not a general-purpose proxy: web traffic is limited to what joining a server needs (see [IP Addresses](/docs/liquidproxy/ip-addresses)).

Each Minecraft name keeps its IP per server, and nobody else gets that IP on that server. See [IP Addresses](/docs/liquidproxy/ip-addresses).

### Connection Ports

Use TCP port **80, 443, 993, 1080 or 25565** with your proxy host. Every port detects the proxy protocol
automatically, so the port does not select HTTP or SOCKS.

### Subscription Plans

| Plan | Networks |
|---|---|
| **Basic** | Dedicated |
| **Pro** | Dedicated and Residential |

- **Dedicated** – Datacenter proxies with low latency. Works on many servers but may be detected by some AntiVPN plugins.
- **Residential** – Residential IP proxies that appear as regular home connections. Required for servers with strict AntiVPN plugins that block datacenter IPs (for example servers using v4Guard or similar).
#### Which plan do I need?

Use the **server checker** on [liquidproxy.net](https://liquidproxy.net) to test your target server:

| Result | Meaning |
|---|---|
| Dedicated network appears sufficient | Basic works. |
| Residential network required | You need Pro. |
| Server cannot be bypassed | No network gets past this server's AntiVPN right now. |
| Geo-IP restricted | The server only allows certain countries; not supported right now. |
| Server not tested yet | Unknown; it may need Residential. |

You can upgrade your subscription at any time through [liquidproxy.net/subscription](https://liquidproxy.net/subscription).

### Setting Up LiquidProxy

LiquidProxy does **not** require a separate download. Once you have an active subscription, open the [dashboard](https://liquidproxy.net/dashboard). The **Connect** card offers two ways to connect. If your client has a Proxy Manager, use Method 1; otherwise use Method 2.

> For a video walkthrough, press **Watch the setup videos** on the dashboard or see the [LiquidProxy setup tutorial](https://www.youtube.com/watch?v=W0dSieDq2qQ).

#### Method 1: Proxy Manager (Recommended)

![Proxy Manager tab of the Connect card](/images/liquidproxy-proxy-manager.png)

1. Pick a **Proxy type**, **Port** and **Location**. **Smart** picks the network that works on each server, **Auto** picks the location closest to you.
2. Copy the **URL** with the copy button. It holds the address, port, username and password, for example `socks5://username:password@smart.eu-fra.liquidproxy.net:1080`. Click one part of the URL to copy only that part.
3. In LiquidBounce, open the **Proxy Manager** and press **Add from Clipboard**. Other proxy managers take the parts one by one.
4. Select the proxy and join your server.

Every port accepts HTTP and SOCKS5. If you can't connect, your network may block that port: pick another one, like 443.

**Regenerate credentials** gives you a new password. The old one stops working right away, so update every proxy manager you use.

For more details on the Proxy Manager in LiquidBounce, see [Using the Proxy Manager](/docs/usage/proxy-manager).

#### Method 2: Minecraft Routes

![Minecraft Routes tab of the Connect card](/images/liquidproxy-minecraft-routes.png)

1. Open the **Minecraft Routes** tab, press **Add route** and enter the server address.
2. Copy the route with its copy button and add it to your Minecraft **server list**.
3. Join it like any other server.

A route added while a location is picked always uses that location. A route added on **Auto** shows **Any location**: its address follows the location picked above, so copy it again after you change the location.

This method works with **any** Minecraft Java Edition client. If a server says "Not authenticated with Minecraft.net", use the Proxy Manager instead.

### Your Dashboard

#### Connections

![Connections card](/images/liquidproxy-connections.png)

The **Connections** card lists your Minecraft games of the last 7 days, newest first. Search it by Minecraft account or server.

- **Green** rows are playing now, with their speed and signal. The power button disconnects them.
- **Yellow** rows are offline accounts whose IP is saved, so they get the same IP next time. The refresh button gives them a new IP on the next join.
- **White** rows are past games.
- Thumbs up or down tells us how a connection went.

Open a row to see how you connected, the server with its address, IP and host, your exit IP, and the web requests made during the game (mostly logins and skins from the game itself).

![Details of a connection](/images/liquidproxy-connection-details.png)

#### Usage

![Usage card](/images/liquidproxy-usage.png)

The **Usage** card shows your playtime, servers joined, Minecraft accounts and exit IPs of the last 7 days.

A route set to **Smart** uses the network the server checker confirmed for that server. If the server has not been verified yet, the dashboard shows which network it falls back to.

### Proxy Locations

LiquidProxy offers a comprehensive network of locations:

- **Europe** – Germany (Frankfurt), France (Gravelines), UK (London), Sweden (Stockholm), Poland (Warsaw), Spain (Madrid)
- **North America** – USA (Los Angeles, Chicago, Seattle, New York, Atlanta), Canada (Beauharnois)
- **South America** – Brazil (São Paulo)
- **Asia** – Singapore

Choose the location closest to the game server you are connecting to for the best latency. The dashboard marks Germany (Frankfurt) and USA (Chicago) as **Recommended**.

### Connection Duration

- **Dedicated network** – You can typically stay connected for up to **one week**.
- **Residential network** – Residential proxies use home connections, and their availability depends on how long these connections remain active. Connections may disconnect unexpectedly due to the nature of residential proxies.

### Connection Limits

LiquidProxy allows up to **2 simultaneous connections** (two Minecraft accounts connected at a time) per subscription. If you see the error:

> "You have reached the maximum number of simultaneous connections."

Wait a few minutes for previous connections to expire, or make sure you have disconnected from other servers before connecting to a new one. For more simultaneous connections, an additional subscription is required.

### Managing Your Subscription

- **Upgrade your plan** – You can upgrade from Basic to Pro at [liquidproxy.net/subscription](https://liquidproxy.net/subscription). You only pay the difference from your existing subscription.
- **Cancel your subscription** – Go to [liquidproxy.net/subscription](https://liquidproxy.net/subscription) and click **Manage Subscription** to cancel.
- **View your account** – Your account details and UID are available at [liquidproxy.net/account](https://liquidproxy.net/account).
- **Session history** – The dashboard lists your recent Minecraft sessions with location, server and IP type.

### Troubleshooting

#### Connection Issues

If you experience frequent disconnections:

1. Try switching to a different proxy **location** on the dashboard.
2. Check that you are using the correct **proxy network** (Dedicated vs. Residential) for the server.
3. Make sure you are connecting with the correct protocol version. Mismatched protocol versions can cause disconnections that are unrelated to LiquidProxy.
4. If the issue persists, contact support with your **UID** (shown at [liquidproxy.net/account](https://liquidproxy.net/account)), the server you are connecting to, and which proxy location and network you are using.

#### Network protocol error when joining a server

This is **not** a LiquidProxy issue. Make sure you are joining with the correct protocol version (for example 26.1.2). You may need to disable **Auto Config** if it is changing your protocol version automatically.

#### Server still detects VPN

- Make sure you are using the **Residential** network if the server has a strict AntiVPN plugin.
- Some servers only allow connections from specific countries. Choose a location in that country. If the server checker reports **Geo-IP restricted**, the server is not supported right now.
- If your IP was detected, press **Change IP on next join** in the session history (see [IP Addresses](/docs/liquidproxy/ip-addresses)). The server may also have put a temporary restriction on your account; try with another account.

#### "Security blocked" on Hypixel

LiquidProxy itself is not blocked by Hypixel. "Security blocked" errors are caused by **low-quality alt accounts**, not by the proxy. Use high-quality alts to resolve this.

#### Subscription not showing

If your subscription does not appear after purchase:

1. Log out and back in at [liquidproxy.net](https://liquidproxy.net).
2. Check that the payment was completed successfully.
3. If the issue persists, contact support through the [contact page](https://ccbluex.net/contact) with your account details.
