## Range

The Range group controls how far you can reach when interacting with or attacking entities. It lets you push your effective reach a little beyond the normal limit, decide whether you can still connect with targets that are partly behind blocks, and add a small scanning buffer so the client starts tracking enemies slightly before they come into hitting distance.

These options are shared, so the same reach behaviour is used everywhere this group appears. Larger values give you a longer reach, which can help you land hits sooner — but very high values are unrealistic and far easier for anti-cheats to flag, so the safer choice is usually a modest increase.

This setting group is used by the following modules:

- [KillAura](/docs/modules/combat/killaura)
- [Reach](/docs/modules/player/reach)

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| RangeIncrease | Decimal | 0.2 | 0.0–5.0 blocks | Extra reach added on top of the normal interaction distance. Higher values let you hit or reach targets from further away, but become increasingly unrealistic and easier to detect. |
| ThroughWallsRange | Decimal | 0.0 | 0.0–8.0 blocks | How far you can still connect with a target that is behind a block or wall. Leave at 0.0 to only hit targets you have a clear line to; raise it to reach enemies through obstacles. |
| ScanRangeIncrease | Decimal Range | 0.0–1.0 | 0.0–7.0 blocks | A randomized extra distance used when scanning for nearby targets, so enemies are picked up slightly before they enter your actual reach. A new value within this range is chosen each time, helping movement feel less robotic. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/combat/killaura/features/KillAuraRange.kt)*
