## AutoWalk

AutoWalk walks for you. It finds a way over hills, around water and cliffs, swims, sneaks along edges and opens doors, trapdoors and fence gates on the way. It also sprints and makes jumps, like across gaps up to four blocks wide, onto fences or up ladders. Use it to travel far without holding the keys.

**Mode** picks where it walks:

- **Forward** walks straight forward.

<video src="/images/modules/autowalk/autowalk-forward.mp4" controls width="600">Your browser does not support the video tag.</video>

- **Direction** keeps walking the way you are looking and goes around water and cliffs.

<video src="/images/modules/autowalk/autowalk-direction.mp4" controls width="600">Your browser does not support the video tag.</video>

- **Goto** walks to a spot you set with [`.goto <x> <y> <z>`](/docs/commands/in-game) and turns off when you get there.

<video src="/images/modules/autowalk/autowalk-goto.mp4" controls width="600">Your browser does not support the video tag.</video>

- **Follow** walks after a player you pick with [`.follow <player>`](/docs/commands/in-game).

<video src="/images/modules/autowalk/autowalk-follow.mp4" controls width="600">Your browser does not support the video tag.</video>

Even if you start facing the wrong way, it turns around and sprints:

<video src="/images/modules/autowalk/autowalk-sprint.mp4" controls width="600">Your browser does not support the video tag.</video>

It sneaks over narrow bridges and through gaps 1.5 blocks high, opens doors and fence gates, swims under walls, prefers ice over soul sand, and reaches far goals bit by bit:

<video src="/images/modules/autowalk/walk-sneak.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/walk-doors.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/walk-swim.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/walk-surfaces.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/walk-staged.mp4" controls width="600">Your browser does not support the video tag.</video>

With **AllowBreak** and **AllowPlace** it may also mine through blocks and place blocks, for example to dig its way out of a cave.

<video src="/images/modules/autowalk/walk-cave.mp4" controls width="600">Your browser does not support the video tag.</video>

With **AllowFly** it flies when you can fly, in creative mode or with [Fly](/docs/modules/movement/fly).

<video src="/images/modules/autowalk/fly-creative.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/fly-module.mp4" controls width="600">Your browser does not support the video tag.</video>

With **AllowElytra** and an elytra on, it glides down to goals below you. With **ElytraRockets** it uses firework rockets to fly to far goals, for example from one End ship to the next. On flat roofs like the Nether roof it bounces along with [ElytraRecast](/docs/modules/movement/elytrarecast), which is much faster than walking.

<video src="/images/modules/autowalk/elytra-glide.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/elytra-end-ships.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/elytra-roof-bounce.mp4" controls width="600">Your browser does not support the video tag.</video>

When you ride a boat or a horse, it steers it for you.

<video src="/images/modules/autowalk/boat-ride.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/horse-ride.mp4" controls width="600">Your browser does not support the video tag.</video>

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Mode | Mode Selector | Forward | Forward, Direction, Goto, Follow | Where AutoWalk walks. |
| Mode → [Goto] → Destination | Position | | | The spot to walk to. `.goto` sets it. |
| Mode → [Follow] → Player | Text | | | Name of the player to follow. `.follow` sets it. |
| Mode → [Follow] → Distance | Decimal | 3.0 | 1.0..10.0 | How close it stays to the player, in blocks. |
| AllowBreak | Toggle | false | | Lets it mine blocks in the way. |
| AllowPlace | Toggle | false | | Lets it place blocks to build a way. |
| AllowParkour | Toggle | true | | Lets it jump across gaps and onto blocks. |
| RiskyJumps | Toggle | false | | Also makes jumps you would not survive if they failed. When off, it only takes jumps with room to spare. |
| MaxFall | Integer | 3 blocks | 0..20 | Highest drop it walks down. |
| PathRange | Integer | 64 blocks | 16..128 | How far ahead it plans a route. Goals further away are reached bit by bit. |
| AllowFly | Toggle | true | | Flies when you are able to fly. |
| AllowElytra | Toggle | true | | Glides with an elytra when you wear one. |
| ElytraRockets | Toggle | true | | Uses firework rockets while gliding to far goals. |
| Rotations | Setting Group | | | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Render | Toggleable Group | On | | Shows the planned route in the world. |
| Render → CanBeCovered | Toggle | false | | Lets blocks hide the route. When off, you see it through walls. |
| Render → Route | Color | | | Color of the route. |
| Render → Search | Color | | | Color shown while it is still looking for a route. |
| Render → Destination | Color | | | Color of the goal. |
| Render → Break | Color | | | Color of blocks it will mine. |
| Render → Place | Color | | | Color of blocks it will place. |
| Render → Target | Color | | | Color of the player or thing it is heading for. |
| Render → Invalid | Color | | | Color of a route that no longer works. |
| Render → Ghost | Toggle | true | | Shows an outline of where you will be next on the route. |
| Render → FadeOut | Integer | 800 ms | 0..3000 | How long the route takes to fade away after you stop. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoWalk.kt)*
