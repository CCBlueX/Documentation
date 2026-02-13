## Using the Proxy Manager

The **Proxy Manager** lets you connect to Minecraft servers through a proxy, allowing you to change your IP address before joining. This is useful for bypassing IP bans or servers running AntiVPN plugins.

### Opening the Proxy Manager

You can open the Proxy Manager from the Title screen:

1. Click **LiquidBounce** on the left side of the Title screen.
2. Select **Proxy Manager** from the menu.

![Proxy Manager](/images/get-started/proxy-manager/proxy-manager-1.png)

### Adding a Proxy

To add a proxy:

1. In the Proxy Manager, click **Add Proxy**.
2. Enter the proxy details:
   - **Host** – The proxy server address (for example `proxy.example.com`).
   - **Port** – The proxy port (for example `1080`).
   - **Username** and **Password** – If your proxy requires authentication.
3. Select the proxy type: **SOCKS5** or **HTTP**.
4. Click **Save** to add the proxy.

![Adding a Proxy](/images/get-started/proxy-manager/proxy-manager-2.png)

### Using a Proxy

Once you have added a proxy:

1. Select the proxy from the list.
2. The proxy will be used for all subsequent server connections.
3. Join a Minecraft server as normal — your connection will be routed through the selected proxy.

To stop using a proxy, click the **Disconnect** button at the bottom left of the Proxy Manager.

![Proxy Connected](/images/get-started/proxy-manager/proxy-manager-3.png)

### Using LiquidProxy

[LiquidProxy](https://liquidproxy.net) is a proxy service designed specifically for Minecraft. It provides dedicated and residential proxies optimized for bypassing AntiVPN plugins and IP ban on Minecraft servers.

If you have a LiquidProxy subscription, you can set it up through the Proxy Manager:

1. Go to [liquidproxy.net](https://liquidproxy.net) to find your proxy credentials.
2. You have two options to connect:
   - **Route Address** – Create a route address on the dashboard and add it directly to your Minecraft server list. No Proxy Manager setup needed.
   - **Proxy Credentials** – Copy your proxy credentials (host, port, username, password) and add them in the Proxy Manager as described above.

> For more details about LiquidProxy, see the [LiquidProxy guide](/docs/tutorials/liquidproxy).
