## AutoWalk

AutoWalk walks for you, so you can cross large terrain without touching the keyboard. It uses LiquidBounce's shared pathfinder, which finds routes over hills and river banks, swims, sneaks along edges and through 1.5 block high gaps, and opens doors, trapdoors and fence gates on the way. Goals beyond the path range or in unloaded chunks are walked in stages. While walking, your head turns the way the walk goes and you sprint.

AutoWalk has the following modes:

- **Forward** — Walks forward.
- **Direction** — Keeps walking in one direction across the terrain.
- **Goto** — Walks to a position set with [`.goto <x> <y> <z>`](/docs/commands/in-game) and turns off on arrival.
- **Follow** — Walks after a player set with [`.follow <player>`](/docs/commands/in-game).

With **AllowBreak** and **AllowPlace**, the route may also mine through blocks and place blocks, for example to dig a shaft up out of a cave and pillar out to the surface.

**Category:** Player
**Enabled by default:** No

---
*Last updated: 2026-11-07 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/nextgen/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoWalk.kt)*
