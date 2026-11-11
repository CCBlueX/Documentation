## Step

Step lets you walk up full blocks without jumping. Some modes can step up even taller walls.

Instant lets you pick how tall a step can be. Legit uses the game's own auto-jump and looks the most normal. Vulcan-2.8.6, BlocksMC and Hypixel-2025-03-11 are made for those anti-cheats and servers. To go down ledges faster, use [ReverseStep](/docs/modules/movement/reversestep).

**Category:** Movement
**Enabled by default:** No

### Settings

Ticks are game steps, 20 per second.

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Instant | Instant, Legit, Vulcan-2.8.6, BlocksMC, Hypixel-2025-03-11 | How you step up. Pick the one that fits the server. |
| Mode → [Instant] → Height | Decimal | 1.0 | 0.6..5.0 | Tallest step you can walk up, in blocks. |
| Mode → [Instant] → Trim | Toggle | false | | Stops the fake jump from going higher than the block you step on. |
| Mode → [Instant] → SimulateJumpOrder | Integer Range | 0..2 | 0..8 | Which parts of a normal jump are sent to the server after a step, so it looks like you jumped. 0..0 sends none. |
| Mode → [Instant] → Wait | Integer Range | 0..0 | 0..60 ticks | How long to wait before the next step. |
| Mode → [Instant] → PacketType | Choice | Full | Full, PositionAndOnGround | What kind of movement messages the fake jump sends. |
| Mode → [BlocksMC] → BaseTimer | Decimal | 3.0 | 0.1..5.0 | Game speed while stepping up. |
| Mode → [BlocksMC] → RecoveryTimer | Decimal | 0.6 | 0.1..5.0 | Game speed right after the step, to even things out. |
| Mode → [Hypixel-2025-03-11] → AlternateBypass | Toggle | false | | Uses another trick for steps taller than 1.25 blocks. |
| Mode → [Hypixel-2025-03-11] → Spoof | Toggle | false | | Tells the server you are on the ground during the step. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/step/ModuleStep.kt)*
