## Clicker

The Clicker setting group controls how and when automated clicks are scheduled. It simulates realistic mouse clicking by distributing a target number of clicks per second (CPS) across a 20-tick cycle using a configurable click pattern technique. Each tick, the clicker determines how many clicks to fire based on the generated click array. If no click has occurred for over 1 second or the item cooldown has elapsed, a click is enforced regardless of the pattern.

The Clicker setting group appears in the following modules:
- [KillAura](/docs/modules/combat/killaura)
- [AutoClicker](/docs/modules/combat/autoclicker)
- [AutoShoot](/docs/modules/combat/autoshoot)
- [TpAura](/docs/modules/combat/tpaura)
- [Scaffold](/docs/modules/world/scaffold)
- [ProjectilePuncher](/docs/modules/world/projectilepuncher)

### Settings

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| CPS | Integer Range | 5..8 | 1..60 | The target clicks per second, specified as a range. A random value within this range is chosen each cycle. The upper bound may vary per module (e.g. Scaffold allows up to 100). |
| Technique | Enum | Stabilized | See [Technique Modes](#technique-modes) | The click pattern used to distribute clicks across the 20-tick cycle. |
| AttackCooldown | Boolean | true | — | Only present when the clicker is bound to the attack key. When enabled, clicks are suppressed while the Minecraft miss cooldown (`missTime`) is active, preventing attacks during the post-miss delay. |

### Technique Modes

**Stabilized** — Distributes clicks evenly across the 20-tick cycle. Calculates a fixed interval between clicks and spreads any remainder across the cycle, resulting in a consistent and uniform click rhythm.

**Efficient** — Ensures at least a one-tick gap between each click by placing clicks at every other tick index. When CPS is below 10, it falls back to the Stabilized pattern to avoid overly wide gaps.

**Spamming** — Simulates normal finger clicking by placing each click at a random tick index in the cycle. This creates an irregular, human-like distribution where multiple clicks can land on the same tick by chance.

**DoubleClick** — Simulates a mouse with a double-click (fire) button. Each click placement adds 2 clicks at a random tick index instead of 1, effectively doubling the actual CPS beyond the configured value.

**Drag** — Simulates drag clicking, where the finger glides across the mouse button. Clicks are concentrated into a burst window of 17–19 ticks (the "travel time"), with the remaining ticks left empty to represent the finger resetting to its starting position. Within the burst window, clicks are distributed to the tick with the fewest clicks first.

**Butterfly** — Simulates butterfly clicking by alternating two fingers on the mouse button. Clicks are placed at random unused tick indices, with each placement adding either 1 or 2 clicks (randomly). Once all indices are used, additional clicks are added to random indices. This produces a pattern similar to DoubleClick but with more randomized variation.

**NormalDistribution** — Generates click timings using a Gaussian (normal) distribution. Uses two frequency bands with different means and standard deviations to model realistic inter-click intervals. Clicks are placed by sampling from these distributions and accumulating time until the cycle is full, producing a statistically natural-looking click pattern.

### ItemCooldown

The ItemCooldown sub-group controls whether the clicker respects the Minecraft attack cooldown (the 1.9+ combat mechanic based on `attackStrengthScale`). When enabled, clicks are only fired once the cooldown progress meets or exceeds the configured minimum threshold.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Minimum | Float Range | 1.0..1.0 | 0.0..2.0 | The minimum cooldown progress required before a click is allowed. A value of 1.0 means the attack must be fully charged. Values above 1.0 add extra wait time beyond a full charge. A random value within this range is selected after each click. |

> **Note:** Not all modules include the ItemCooldown sub-group. Modules that use the use key (e.g. AutoShoot, Scaffold) or do not need cooldown management (e.g. ProjectilePuncher) create their Clicker without an ItemCooldown.

---
*Last updated: 2026-02-13*
