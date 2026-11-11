## Eagle

Eagle sneaks for you when you get close to the edge of a block, so you don't fall off. Use it when you build bridges by hand: you walk backwards and place blocks, and Eagle sneaks right at the edge. It is a gentler choice than [Scaffold](/docs/modules/world/scaffold), which places the blocks for you.

**Category:** Player
**Enabled by default:** No
**Aliases:** FastBridge, BridgeAssistant, LegitScaffold

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| EdgeDistance | Decimal Range | 0.4..0.6 | 0.01..1.3 | How close to the edge you get before it sneaks. Smaller lets you go further out. A new random value from the range is used after each sneak. |
| Conditional | Toggleable Group | On | | Eagle only sneaks when the conditions below are met. Turn it off to sneak at every edge. |
| Conditional → Conditions | Multi-Select | OnGround | Left, Right, Forwards, Backwards, HoldingBlocks, OnGround, Sneak | All selected conditions must be true: walking that way, holding blocks, standing on the ground, or holding the sneak key. With Sneak, Eagle only works while you hold sneak, and then stops sneaking for you away from the edge. |
| Conditional → Pitch | Decimal Range | -90.0..90.0 | -90.0..90.0 | Only sneaks while you look up or down within this range. For example, set it to 60..90 to only sneak while looking down. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/player/ModuleEagle.kt)*
