## In-Game Commands

These commands work while you are in a world. They show information about you and the server, and move you around.

---

### `.ping`

Shows your ping to the server in milliseconds. Lower is better.

```
.ping
```

---

### `.tps`

Shows how fast the server is running, in ticks per second. A server without lag runs at 20. Some servers change how time is sent, so the number can be wrong there.

```
.tps
```

---

### `.center`

Moves you to the middle of the block you are standing on.

```
.center
```

---

### `.teleport`

Teleports you to a position. Short form: `.tp`. The [Teleport](/docs/global-settings/teleport) settings change how it teleports.

```
.teleport <x> <y> <z> [highTp]
```

- `x y z`: the position, written like in Minecraft's own `/tp`. Plain numbers (`100 64 -200`) are a fixed spot. `~` counts from where you are (`~ ~10 ~` is 10 blocks up). `^` counts from where you look (`^ ^ ^5` is 5 blocks forward).
- `highTp`: add `true` to use the HighTPAmount height from the Teleport settings instead of your `y`.

```
.teleport 100 64 200
.tp ~ ~10 ~
.tp ^ ^ ^5
.tp 0 0 0 true
```

---

### `.playerteleport`

Teleports you to another player. Short forms: `.playertp`, `.ptp`. The [Teleport](/docs/global-settings/teleport) settings change how it teleports.

```
.playerteleport <player> [copy]
```

- `player`: a player near enough that your game has loaded them, even if the tab list hides them.
- `copy`: write `copy` to not teleport and instead copy a `.teleport` command to that player's position, so you can paste it later.

```
.ptp Steve
.ptp Steve copy
```

---

### `.vclip`

Moves you straight up or down, through blocks. If you are riding something, it moves that too. The [Teleport](/docs/global-settings/teleport) settings change how it teleports.

- `.vclip by <distance>`: moves you this many blocks. Positive numbers go up, negative numbers go down.
- `.vclip smart up [max]`: moves you up onto the next block you can stand on, at most `max` blocks away (10 if you leave it out).
- `.vclip smart down [max]`: the same, but downward.

```
.vclip by 5
.vclip by -10
.vclip smart up
.vclip smart down 20
```

---

### `.goto`

Walks you to a position with [AutoWalk](/docs/modules/player/autowalk). You write the position the same way as for `.teleport`.

```
.goto <x> <y> <z>
```

```
.goto 100 64 200
.goto ~ ~ ~50
```

---

### `.follow`

Walks after a player with [AutoWalk](/docs/modules/player/autowalk).

```
.follow <player>
```

The player has to be near enough that your game has loaded them.

---

### `.coordinates`

Shows, copies or shares your position. Short forms: `.coords`, `.position`.

- `.coordinates info`: shows your position and dimension in chat.
- `.coordinates copy`: copies them, so you can paste them somewhere.
- `.coordinates whisper <player>`: sends them to a player as a private message.

```
.coords info
.coords whisper Steve
```

---

### `.username`

Shows your Minecraft name and copies it.

```
.username
```

---

### `.say`

Sends a chat message to the server as it is, even if it starts with the command prefix.

```
.say <message>
```

`.say .help` sends ".help" to the chat instead of running the help command.

---

### `.serverinfo`

Shows what the client knows about the server you are on: its address, version, brand, TPS, ping and which anti-cheat it seems to use. Click a line to copy it.

```
.serverinfo [detect...]
```

- `detect`: `Plugins` also tries to find out which plugins the server has. `Hosting` also tries to find out who hosts the server. You can use both.

```
.serverinfo
.serverinfo Plugins
.serverinfo Plugins Hosting
```

---

### `.remoteview`

Lets you see through another player's eyes. Short form: `.rv`.

- `.remoteview view <player>`: looks from that player.
- `.remoteview off`: goes back to your own view.

```
.rv view Steve
.rv off
```

---

### `.map_image`

Turns the map you are holding into a picture.

- `.map_image copy`: copies the picture, so you can paste it into another program.
- `.map_image save [filename]`: saves it as a PNG file in the `map_image` folder inside your LiquidBounce folder. Click the file name in chat to open it.

---

### `.fakeplayer`

Spawns pretend players that only you can see. They are handy for testing combat modules like KillAura.

- `.fakeplayer spawn [name]`: spawns one where you stand.
- `.fakeplayer remove [name]`: removes one.
- `.fakeplayer clear`: removes all of them.
- `.fakeplayer startrecording`: starts recording how you move.
- `.fakeplayer endrecording [name]`: stops recording and spawns a fake player that repeats your movement.

The name is `FakePlayer` if you leave it out.

```
.fakeplayer spawn Dummy
.fakeplayer startrecording
.fakeplayer endrecording
.fakeplayer clear
```

---

*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/command/commands/ingame)*
