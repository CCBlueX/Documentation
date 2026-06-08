## StrongholdFinder

Tracks your Eye of Ender throws and predicts the most likely stronghold chunk, then draws the candidate chunks and announces its best guess. Throw eyes from two or more different positions and the module triangulates where the stronghold is — no manual coordinate math or external calculators required.

**Category:** World
**Enabled by default:** No

### How to use

1. Enable the module.
2. Throw an Eye of Ender and watch it fly.
3. Walk a short distance sideways and throw another eye.
4. The predicted stronghold chunk is highlighted in the world and printed in chat. More throws from spread-out positions improve accuracy.

### Settings

Below is the complete tree of all configurable settings for this module.

```
├── Sigma (Decimal | default: 0.03 | range: 0.005..0.2 | °)
├── HypothesisCount (Integer | default: 20000 | range: 2000..100000)
├── RequireSameStrongholdAcrossThrows (Toggle | default: true)
├── SampleDelayTicks (Integer | default: 2 | range: 0..10)
├── MinEyeHorizontalSpeed (Decimal | default: 0.02 | range: 0.001..0.2)
├── MaxSampleAgeTicks (Integer | default: 20 | range: 5..100)
├── ShowTopCandidates (Integer | default: 3 | range: 1..10)
├── RenderRays (Toggle | default: true)
├── RenderBestChunk (Toggle | default: true)
├── RenderTopChunks (Toggle | default: true)
├── AnnouncePrediction (Toggle | default: true)
└── ResetOnWorldChange (Toggle | default: true)
```

### Settings Details

- **Sigma** (Decimal) — default: `0.03`; range: `0.005` – `0.2`; unit: ° — Assumed angular error of each eye throw. Larger values widen the search if your throws are imprecise.
- **HypothesisCount** (Integer) — default: `20000`; range: `2000` – `100000` — Number of candidate points sampled when estimating the stronghold. Higher is more accurate but more demanding.
- **RequireSameStrongholdAcrossThrows** (Toggle) — default: `true` — Only combine throws that point at the same stronghold, avoiding mixed predictions.
- **SampleDelayTicks** (Integer) — default: `2`; range: `0` – `10` — Ticks to wait after a throw before sampling its direction.
- **MinEyeHorizontalSpeed** (Decimal) — default: `0.02`; range: `0.001` – `0.2` — Minimum horizontal eye speed required for a throw to be recorded as a sample.
- **MaxSampleAgeTicks** (Integer) — default: `20`; range: `5` – `100` — How long a throw sample stays valid before being discarded.
- **ShowTopCandidates** (Integer) — default: `3`; range: `1` – `10` — How many of the best chunk candidates to display.
- **RenderRays** (Toggle) — default: `true` — Draw the direction ray of each recorded eye throw.
- **RenderBestChunk** (Toggle) — default: `true` — Highlight the single most likely chunk.
- **RenderTopChunks** (Toggle) — default: `true` — Highlight the top candidate chunks.
- **AnnouncePrediction** (Toggle) — default: `true` — Print the predicted chunk and its probability in chat.
- **ResetOnWorldChange** (Toggle) — default: `true` — Clear all collected samples when you change worlds or dimensions.

### Screenshots

*Screenshots for StrongholdFinder will be added in a future update.*

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfc/src%2Fmain%2Fkotlin%2Fnet%2Fccbluex%2Fliquidbounce%2Ffeatures%2Fmodule%2Fmodules%2Fworld%2FModuleStrongholdFinder.kt)*
