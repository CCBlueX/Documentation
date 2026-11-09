## AutoWalk

AutoWalk walks for you, so you can cross large terrain without touching the keyboard. It uses LiquidBounce's shared pathfinder, which finds routes over hills and river banks, swims, sneaks along edges and through 1.5 block high gaps, and opens doors, trapdoors and fence gates on the way. Goals beyond the path range or in unloaded chunks are walked in stages. While walking, your head turns the way the walk goes and you sprint, sprint-hopping along straight runs.

Routes also include jumps, worked out by simulating your movement tick by tick: sprint jumps at any angle, up a block, down several, across gaps up to four blocks wide, into holes in walls, onto fences, panes and walls, under low ceilings and onto ladders. While following the route, each jump is worked out again every tick from where you really are. By default, jumps need room to spare and are only taken when they save time; with **RiskyJumps**, the route also takes jumps where a miss would not be survived.

AutoWalk has the following modes:

- **Forward** — Walks forward.

<video src="/images/modules/autowalk/autowalk-forward.mp4" controls width="600">Your browser does not support the video tag.</video>

- **Direction** — Keeps walking in one direction across the terrain, aiming far ahead so water and cliffs are walked around.

<video src="/images/modules/autowalk/autowalk-direction.mp4" controls width="600">Your browser does not support the video tag.</video>

- **Goto** — Walks to a position set with [`.goto <x> <y> <z>`](/docs/commands/in-game) and turns off on arrival.

<video src="/images/modules/autowalk/autowalk-goto.mp4" controls width="600">Your browser does not support the video tag.</video>

- **Follow** — Walks after a player set with [`.follow <player>`](/docs/commands/in-game).

<video src="/images/modules/autowalk/autowalk-follow.mp4" controls width="600">Your browser does not support the video tag.</video>

Started facing away, the head turns the way the walk goes and it sprints:

<video src="/images/modules/autowalk/autowalk-sprint.mp4" controls width="600">Your browser does not support the video tag.</video>

Sneaking over a narrow bridge and through a gap 1.5 blocks high, opening a door and a fence gate, swimming under a wall, taking ice over soul sand, and a goal 160 blocks away walked in stages:

<video src="/images/modules/autowalk/walk-sneak.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/walk-doors.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/walk-swim.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/walk-surfaces.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/walk-staged.mp4" controls width="600">Your browser does not support the video tag.</video>

With **AllowBreak** and **AllowPlace**, the route may also mine through blocks and place blocks, for example to dig a shaft up out of a cave and pillar out to the surface.

<video src="/images/modules/autowalk/walk-cave.mp4" controls width="600">Your browser does not support the video tag.</video>

With **AllowFly**, AutoWalk flies the route when you can fly, in creative or with [Fly](/docs/modules/movement/fly).

<video src="/images/modules/autowalk/fly-creative.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/fly-module.mp4" controls width="600">Your browser does not support the video tag.</video>

With **AllowElytra** and an elytra worn, it glides down to goals below, and with **ElytraRockets** it cruises to far goals with firework rockets, for example from one End city ship to the next. Along flat roofs such as the Nether roof it bounces with [ElytraRecast](/docs/modules/movement/elytrarecast), much faster than walking.

<video src="/images/modules/autowalk/elytra-glide.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/elytra-end-ships.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/elytra-roof-bounce.mp4" controls width="600">Your browser does not support the video tag.</video>

Riding a boat or a horse, it steers the mount instead.

<video src="/images/modules/autowalk/boat-ride.mp4" controls width="600">Your browser does not support the video tag.</video>
<video src="/images/modules/autowalk/horse-ride.mp4" controls width="600">Your browser does not support the video tag.</video>

**Category:** Player
**Enabled by default:** No

---
*Last updated: 2026-11-07 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoWalk.kt)*
