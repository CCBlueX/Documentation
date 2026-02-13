## LiquidProxy

[LiquidProxy](https://liquidproxy.net) is a proxy service built specifically for Minecraft. It allows you to change your IP address when connecting to Minecraft servers, which is useful for bypassing IP bans and servers running AntiVPN plugins.

> LiquidProxy is a separate paid service. You can subscribe at [liquidproxy.net](https://liquidproxy.net).

### How LiquidProxy Works

LiquidProxy routes your Minecraft connection through proxy servers so that the game server sees a different IP address instead of your real one. Unlike a traditional VPN, LiquidProxy only affects your Minecraft connection and is optimized to minimize latency.

LiquidProxy operates on a **fair-use** basis. As long as your traffic is normal Minecraft usage, there is no limit on IPs or data transfer (GBs). LiquidProxy is **only** for Minecraft Java Edition — it is not a general-purpose proxy and will reject non-Minecraft traffic.

### Subscription Plans

LiquidProxy offers two types of proxy networks:

- **Dedicated** – Datacenter proxies with low latency. Works on many servers but may be detected by some AntiVPN plugins. Your IP is never shared with other users on the same server.
- **Residential** – Residential IP proxies that appear as regular home connections. Required for servers with strict AntiVPN plugins that block datacenter IPs (for example servers using v4Guard or similar).

#### Which plan do I need?

Use the **server checker** on [liquidproxy.net](https://liquidproxy.net) to test whether your target server requires Dedicated or Residential. As a general rule:

- If the server checker says **Dedicated is sufficient**, the cheaper Dedicated plan will work.
- If the server checker says **Residential required** or the server has not been tested, you may need the Residential plan.
- Servers that restrict connections to specific countries or regions typically require Residential.

You can upgrade your subscription at any time through [liquidproxy.net/subscription](https://liquidproxy.net/subscription).

### Setting Up LiquidProxy

LiquidProxy does **not** require a separate download. Once you have an active subscription:

1. Log in at [liquidproxy.net](https://liquidproxy.net).
2. Choose a **location** (for example Frankfurt, London, Los Angeles).
3. Connect using one of two methods:

> For a video walkthrough, see the [LiquidProxy setup tutorial](https://www.youtube.com/watch?v=W0dSieDq2qQ).

#### Method 1: Route Address (Recommended)

1. On the LiquidProxy dashboard, create a **route address** for your target server.
2. Copy the route address.
3. In Minecraft, add it to your **server list** as a new server.
4. Join the server through the route address — your connection will automatically be proxied.

This method works with **any** Minecraft Java Edition client and does not require a Proxy Manager.

#### Method 2: Proxy Credentials

1. On the LiquidProxy dashboard, copy your **proxy credentials** (host, port, username, password).
2. In a client with a Proxy Manager (such as LiquidBounce), open the **Proxy Manager** and add a new proxy with the credentials from the dashboard.
3. Select the proxy and join your target server normally.

For more details on using the Proxy Manager in LiquidBounce, see [Using the Proxy Manager](/docs/usage/proxy-manager).

### Proxy Locations

LiquidProxy offers a comprehensive network of locations:

- **Europe** – Germany (Frankfurt), France (Gravelines), UK (London), Sweden (Stockholm), Poland (Warsaw), Spain (Madrid)
- **North America** – USA (Los Angeles, Chicago, Seattle, New York, Atlanta), Canada (Beauharnois)
- **South America** – Brazil (São Paulo)
- **Asia** – Singapore

Choose the location closest to the game server you are connecting to for the best latency.

### Connection Duration

- **Dedicated network** – You can stay connected for up to **one week**.
- **Residential network** – Residential proxies use home connections, and their availability depends on how long these connections remain active. Connections may disconnect unexpectedly due to the nature of residential proxies.

### Connection Limits

LiquidProxy allows up to **2 simultaneous connections** (two Minecraft accounts connected at a time) per subscription. If you see the error:

> "You have reached the maximum number of simultaneous connections."

Wait a few minutes for previous connections to expire, or make sure you have disconnected from other servers before connecting to a new one. For more simultaneous connections, an additional subscription is required.

### Managing Your Subscription

- **Upgrade your plan** – You can upgrade from Dedicated to Residential at [liquidproxy.net/subscription](https://liquidproxy.net/subscription). You only pay the difference from your existing subscription.
- **Cancel your subscription** – Go to [liquidproxy.net/subscription](https://liquidproxy.net/subscription) and click **Manage Subscription** to cancel.
- **View your account** – Your account details and UID are available at [liquidproxy.net/account](https://liquidproxy.net/account).

### Troubleshooting

#### Connection Issues

If you experience frequent disconnections:

1. Try switching to a different proxy **location** on the dashboard.
2. Check that you are using the correct **proxy network** (Dedicated vs. Residential) for the server.
3. Make sure you are connecting with the correct protocol version. Mismatched protocol versions can cause disconnections that are unrelated to LiquidProxy.
4. If the issue persists, contact support with your **UID** (shown at [liquidproxy.net/account](https://liquidproxy.net/account)), the server you are connecting to, and which proxy location and network you are using.

#### Network protocol error when joining a server

This is **not** a LiquidProxy issue. Make sure you are joining with the correct protocol version (for example 1.21.11). You may need to disable **Auto Config** if it is changing your protocol version automatically.

#### Server still detects VPN

- Make sure you are using the **Residential** network if the server has a strict AntiVPN plugin.
- Some servers use geo-restrictions (only allowing connections from specific countries). Residential proxies can typically bypass these, but dedicated proxies may not.
- If you recently switched IPs from e.g. a detected IP, the server may have put a temporary restriction on your account. Try with another account.

#### "Security blocked" on Hypixel

LiquidProxy itself is not blocked by Hypixel. "Security blocked" errors are caused by **low-quality alt accounts**, not by the proxy. Use high-quality alts to resolve this.

#### Subscription not showing

If your subscription does not appear after purchase:

1. Log out and back in at [liquidproxy.net](https://liquidproxy.net).
2. Check that the payment was completed successfully.
3. If the issue persists, contact support through the [contact page](https://ccbluex.net/contact) with your account details.
