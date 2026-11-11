## StrongholdFinder

StrongholdFinder helps you find a stronghold with Eyes of Ender. Throw an eye in the Overworld, then walk a bit to the side and throw another. Each throw makes the guess better.

It draws a line for each throw and colors the best chunk blue and the next best ones orange. In the middle of your screen it shows the coordinates of the best chunk. When you get close and the game shows you the End Portal frame, it highlights it and points to it. Turning the module off clears all throws.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Sigma | Decimal | 0.03 | 0.005..0.2 ° | How much each throw may be off. Raise it if the guess jumps around. |
| HypothesisCount | Integer | 20000 | 2000..100000 | How many possible places it checks. Higher is more exact but slower. |
| RequireSameStrongholdAcrossThrows | Toggle | true | | All throws must point to the same stronghold. Leave on for normal play. |
| SampleDelayTicks | Integer | 2 | 0..10 ticks | Wait after the eye appears before reading its direction (20 ticks per second). |
| MinEyeHorizontalSpeed | Decimal | 0.02 | 0.001..0.2 | Eyes slower than this are ignored. |
| MaxSampleAgeTicks | Integer | 20 | 5..100 ticks | How long after your throw the eye may appear and still count. |
| MaxEyeSpawnDistance | Decimal | 8.0 | 1.0..32.0 blocks | How far from you the eye may appear. Eyes thrown by other players are ignored. |
| ShowTopCandidates | Integer | 3 | 1..10 | How many of the best chunks to show. |
| RenderRays | Toggle | true | | Draws a line for each throw. |
| RenderBestChunk | Toggle | true | | Colors the best chunk blue. |
| RenderTopChunks | Toggle | true | | Colors the next best chunks orange. |
| AnnouncePrediction | Toggle | true | | Shows a message when the best guess changes. |
| ResetOnWorldChange | Toggle | true | | Clears all throws when you change worlds. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleStrongholdFinder.kt)*
