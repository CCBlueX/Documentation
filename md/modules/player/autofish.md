## AutoFish

AutoFish takes care of fishing for you. While you hold a fishing rod, it listens for the splash that means a fish is biting and automatically reels in your line, so you can AFK-fish without watching the screen. After a catch it can recast the rod for you, keeping the cycle going indefinitely.

By default it triggers on the vanilla bobber-splash sound. On servers that use custom fishing setups you can add their sounds in the **Sounds** list, and the **SoundDistance** check helps avoid false catches by ignoring splash sounds that come from somewhere other than your own bobber. Enable **AutoCastRod** if you want it to throw the line out the first time as well, not just recast after a catch. Pairs well with [AntiAFK](/docs/modules/player/antiafk) for long unattended sessions.

**Category:** Player
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ReelDelay | Integer Range | 5..8 | 0..20 | How long (in ticks) to wait after a bite before reeling in, picked randomly within this range to look more natural. |
| Sounds | Registry List | — | — | The sound events that count as a fish biting and trigger a reel-in. Add custom server sounds here if the default splash isn't detected. |
| SoundDistance | Toggleable Group | on | — | When on, only reels in if the triggering sound comes from close to your bobber, preventing false catches from other players' fishing. |
| SoundDistance → MaxDistance | Decimal | 1.0 | 0.0..10.0 | Maximum distance (in blocks) between your bobber and the sound for it to count as your catch. |
| RecastRod | Toggleable Group | on | — | When on, automatically throws the rod back out after reeling in a fish. |
| RecastRod → Delay | Integer Range | 15..20 | 10..30 | How long (in ticks) to wait before recasting, picked randomly within this range. |
| AutoCastRod | Toggleable Group | off | — | When on, automatically casts the rod when no line is in the water, so fishing starts without a manual throw. |
| AutoCastRod → Delay | Integer Range | 15..20 | 0..30 | How long (in ticks) to wait before auto-casting, picked randomly within this range. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleAutoFish.kt)*
