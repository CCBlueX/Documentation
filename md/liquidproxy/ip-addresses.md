## IP Addresses

To get a new IP for a server, open **Connections** on the [dashboard](https://liquidproxy.net/dashboard)
and press **New IP on next join** on that game. Your next join gets a different IP.

### Your IP stays the same

When you join a server, LiquidProxy keeps that IP for your Minecraft name on that server and location. Every
later join with the same name gets the same IP, so the server sees one consistent player.

- The IP belongs to the Minecraft name, not to your LiquidProxy account. Joining with the same name from
  another LiquidProxy account at the same location gives the same IP.
- Servers that belong together (for example several domains of one network) count as one server.
- Different servers and different locations get their own IP.

You keep the IP until one of these happens:

1. You don't join that server with that name for 3 days.
2. You press **New IP on next join**.
3. The IP stops working, goes offline or becomes much slower than when you got it.

In all three cases your next join picks a new IP automatically.

### Nobody else gets your IP

While an IP is yours on a server, no other player gets it there. After you give it up, it stays unused on
that server for a while, for everyone, so a detected or banned IP does not come back to you or anyone else.
The IP can still be used on other servers.

### Web traffic

LiquidProxy is made for Minecraft Java Edition. Web traffic through the proxy is only meant for what joining
a server needs, such as server verification and captcha pages, Mojang login and resource packs; most other
sites are blocked.

Web requests don't get an IP of their own. They use the IP of your current or last Minecraft session at that
location, so a verification page sees the same IP as the server.
