## AirJump

AirJump lets you jump again while you're already off the ground, giving you extra height or a second boost without touching solid ground. It's handy for reaching ledges, crossing small gaps, or stringing together moves that a normal single jump can't pull off.

The behavior depends on the selected **Mode**. *JumpFreely* removes the limit entirely, so you can keep jumping in the air as many times as you like. *DoubleJump* grants exactly one extra jump after leaving the ground, resetting once you land again. *GhostBlock* lets you stand on an invisible block while holding the jump key, so you can hover or climb upward as long as you keep jumping.

Because this gives obvious non-vanilla movement, it can look suspicious on servers with strict anti-cheat. Pair it with modules like [HighJump](/docs/modules/movement/highjump) or [Fly](/docs/modules/movement/fly) for more dramatic vertical mobility.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Choice | GhostBlock | JumpFreely, DoubleJump, GhostBlock | How the mid-air jump works: *JumpFreely* allows unlimited air jumps, *DoubleJump* grants one extra jump per landing, and *GhostBlock* places an invisible block under you while you hold the jump key. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleAirJump.kt)*
