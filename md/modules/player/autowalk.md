## AutoWalk

AutoWalk holds your forward movement key for you, so your character keeps walking in whatever direction you're looking without you needing to touch the keyboard. Turn it on, point your camera where you want to go, and you'll keep moving forward; turn your view and you turn your path.

It's handy for long, repetitive treks — crossing large terrain, AFK pathing, or holding a steady walking direction while you focus on aiming or interacting. Under the hood it simply forces the "forwards" input on every [movement input event](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoWalk.kt#L35-L37), so it stacks with your normal controls — you can still strafe, sprint, jump, and steer with the mouse as usual. It does not pathfind or avoid hazards, so it will happily walk you off a ledge or into a wall if you stop steering.

**Category:** Player
**Enabled by default:** No

### Settings

This module has no configurable settings.

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoWalk.kt)*
