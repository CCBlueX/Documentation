## StrongholdFinder

StrongholdFinder automates the process of locating a stronghold by tracking the direction Eyes of Ender fly when thrown. Each time you throw an Eye of Ender in the Overworld, the module records your position and the angle the eye travels, then uses a Bayesian statistical estimator to combine all collected measurements into a probability distribution over every possible stronghold chunk. With enough throws from different positions, the top candidate converges on the chunk containing the stronghold entrance.

Once the module has at least one measurement, it renders direction rays from each throw point and highlights the most likely stronghold chunk(s) directly in the world — the best candidate appears in blue, runner-up chunks in orange. A HUD overlay near the center of your screen shows the best chunk's coordinates, its estimated probability, and a ready-to-paste `/tp` command. If you actually walk close enough to load the chunk and the game sends End Portal Frame or End Portal blocks to your client, the module switches automatically to a portal-detection display that highlights those blocks and draws a line pointing to the nearest one, making the final approach straightforward.

The module resets all collected measurements when you disable it or (optionally) when you change worlds, so you always start fresh on a new seed. Precision-tuning options let you balance accuracy against computation cost: `Sigma` controls how much angular error is assumed per throw, and `HypothesisCount` sets how many candidate stronghold positions are sampled internally — higher values are more accurate but take more time to compute after each throw.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Sigma | Decimal | 0.03 | 0.005 – 0.2 ° | Assumed standard deviation of your throw angle in degrees. Lower values trust each measurement more; raise it if your throws feel imprecise. |
| HypothesisCount | Integer | 20000 | 2000 – 100000 | Number of stronghold position hypotheses sampled for the Bayesian estimator. Higher values increase accuracy at the cost of recalculation time. |
| RequireSameStrongholdAcrossThrows | Toggle | true | — | When enabled, all measurements must agree on a single stronghold rather than allowing each throw to point to a different one. Recommended for normal gameplay. |
| SampleDelayTicks | Integer | 2 | 0 – 10 | How many ticks after an Eye of Ender spawns before its direction is sampled. A small delay lets the eye stabilize before its angle is recorded. |
| MinEyeHorizontalSpeed | Decimal | 0.02 | 0.001 – 0.2 | Minimum horizontal speed (blocks/tick) an eye must have for its direction to be recorded. Filters out eyes that have already slowed or are falling. |
| MaxSampleAgeTicks | Integer | 20 | 5 – 100 | Maximum age (in ticks) of a pending throw before it is discarded. If the eye entity spawns too long after the throw action, the pairing is dropped. |
| ShowTopCandidates | Integer | 3 | 1 – 10 | How many of the highest-probability stronghold chunks to display in the world render and on-screen overlay. |
| RenderRays | Toggle | true | — | Draws a direction ray from each recorded throw position toward the predicted stronghold direction. |
| RenderBestChunk | Toggle | true | — | Highlights the top-ranked stronghold chunk candidate in the world (shown in blue). |
| RenderTopChunks | Toggle | true | — | Highlights runner-up stronghold chunk candidates in the world (shown in orange). |
| AnnouncePrediction | Toggle | true | — | Sends a client notification whenever the best chunk prediction changes after a new measurement is recorded. |
| ResetOnWorldChange | Toggle | true | — | Clears all measurements and predictions when you change worlds or reconnect, preventing data from a previous seed carrying over. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleStrongholdFinder.kt)*
