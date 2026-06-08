## Step

Step lets you walk up full blocks — and taller obstacles, depending on the mode — without needing to jump manually. Whenever you walk into a ledge, the module handles the upward movement for you automatically, keeping your traversal fluid and uninterrupted.

**Legit** works with vanilla auto-jump and looks the most natural of the available options. **Instant** overrides your step height directly and can optionally send a series of jump-arc packets afterward to mask the movement from anticheats. **Vulcan286** is tuned for the Vulcan anticheat around version 2.8.6, **BlocksMC** targets the BlocksMC network using a timer-based approach, and **Hypixel** uses a jump-velocity sequence designed for Hypixel's anticheat with optional ground-state spoofing.

If you also want to descend ledges more quickly rather than drifting down naturally, take a look at [ReverseStep](/docs/modules/movement/reversestep).

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Legit | — | Stepping implementation to use. Options: Instant, Legit, Vulcan286, BlocksMC, Hypixel. Pick the one that matches your server's anticheat. |
| Mode → [Instant] → Height | Decimal | 1.0 | 0.6..5.0 | Maximum block height that can be stepped up in a single movement. |
| Mode → [Instant] → Trim | Toggle | false | — | Caps the simulated jump Y position to the actual step destination, preventing the player from visibly overshooting the block. |
| Mode → [Instant] → SimulateJumpOrder | Integer Range | 8..8 | 0..8 | Range of jump-arc packets sent after each step to mimic natural jump motion and reduce anticheat flags. Set to 0..0 to skip packet simulation entirely. |
| Mode → [Instant] → Wait | Integer Range | 5..5 | 0..60 | Cooldown between consecutive step operations, in ticks. |
| Mode → [Instant] → PacketType | Choice | Full | — | Format of the movement packets sent during jump simulation. Options: PositionAndOnGround, Full. |
| Mode → [BlocksMC] → BaseTimer | Decimal | 4.0 | 0.1..5.0 | Timer speed multiplier applied at the start of the step sequence. |
| Mode → [BlocksMC] → RecoveryTimer | Decimal | 0.8 | 0.1..5.0 | Timer speed multiplier applied during the recovery phase after the step completes. |
| Mode → [Hypixel] → AlternateBypass | Toggle | true | — | Uses an alternate bypass strategy for taller steps (above 1.25 blocks) when the standard jump sequence is not sufficient. |
| Mode → [Hypixel] → Spoof | Toggle | true | — | Spoofs the ground-state flag in movement packets to assist with bypassing Hypixel's anticheat detection. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/step/ModuleStep.kt)*
