## Anchor

Anchor is a movement aid for crystal PvP that automatically pulls you down into nearby safe holes — the 1×1 spots where you can't be hit by exploding end crystals from the side. Hold the module's bind and Anchor scans for valid holes around you, then gently steers your movement toward the closest one and drops you in. Once you're inside a hole, it keeps you centered so you stay protected.

You'd use this when you need to snap into cover fast during a crystal fight without manually walking and dropping into the exact tile. It only looks for holes at or below your feet, so it pulls you down rather than trying to lift you. The bind works as a hold action, and the module turns itself off when you leave the world.

Use **MaxDistance** to control how far Anchor will reach for a hole, and the speed settings to tune how aggressively it moves you horizontally and vertically. Pairs naturally with [CrystalAura](/docs/modules/combat/crystalaura), [Surround](/docs/modules/world/surround), and [HoleESP](/docs/modules/render/holeesp).

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MaxDistance | Decimal | 4.0 | 0.1..6.0 | How far away (in blocks) a hole can be for Anchor to consider pulling you into it. |
| HorizontalSpeed | Decimal | 0.3 | 0.0..10.0 | How fast you are moved sideways toward the hole. Set to 0 to stop pulling and only prevent you from sliding out once you're over the hole. |
| VerticalSpeed | Decimal | 0.1 | 0.0..10.0 | How fast you are pulled downward into the hole. Set to 0 to leave your vertical movement untouched. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleAnchor.kt)*
