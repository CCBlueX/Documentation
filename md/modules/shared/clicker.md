## Clicker

The Clicker setting group controls how and when automated clicks are scheduled. Presses are planned ahead in milliseconds by the selected click timing technique and then batched into ticks, the same way Minecraft drains every click queued since the previous tick. Because the presses are known in advance, other features can predict upcoming clicks and act accordingly. While an item cooldown is in use, one click is enforced on the tick the cooldown fills up.

Consecutive presses form a combo. When planned presses go unused for a while, or the game skips ticks, the combo ends and a new one starts with a fresh press.

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
| CPS | Integer Range | 11..14 | 1..30 | The target clicks per second, specified as a range. The upper bound may vary per module (e.g. Scaffold allows up to 100). |
| Technique | Enum | Human | See [Technique Modes](#technique-modes) | The timing used to decide how long to wait between two presses. |
| MaxPerTick | Integer | 2 | 1..5 clicks | The highest number of clicks a single tick may consume. Presses that would exceed this are pushed to a later tick. |
| MissCooldown | Boolean | true | — | Only present when the clicker is bound to the attack key. When enabled, clicks are dropped while the Minecraft miss cooldown (`missTime`) is active, preventing attacks during the post-miss delay. |

### Technique Modes

**Human** — Derives each interval from the intervals already clicked in the current combo and from how long the combo has been running, so the click rhythm varies and drifts the way a real hand does.

**Constant** — Spaces presses evenly at the top of the CPS range, for anti-cheats that only look at the time since the last attack.

### ItemCooldown

The ItemCooldown sub-group controls whether the clicker respects the Minecraft attack cooldown (the 1.9+ combat mechanic based on `attackStrengthScale`). When enabled, clicks are only fired once the cooldown progress meets or exceeds the configured minimum threshold.

| Setting | Type | Default | Range | Description |
|---------|------|---------|-------|-------------|
| Minimum | Float Range | 1.0..1.0 | 0.0..2.0 | The minimum cooldown progress required before a click is allowed. A value of 1.0 means the attack must be fully charged. Values above 1.0 add extra wait time beyond a full charge. A random value within this range is selected after each click. |

> **Note:** Not all modules include the ItemCooldown sub-group. Modules that use the use key (e.g. AutoShoot, Scaffold) or do not need cooldown management (e.g. ProjectilePuncher) create their Clicker without an ItemCooldown.

---
*Last updated: 2026-09-23*
