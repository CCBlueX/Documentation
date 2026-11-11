## Anchor

Anchor pulls you into a nearby safe hole during crystal PvP. A safe hole is a one block gap with blocks around it, so crystals can't hit you from the side. Anchor only looks for holes at your feet or below you, and it keeps you in the middle of the hole once you are in.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MaxDistance | Decimal | 4.0 | 0.1..6.0 | How far away a hole can be, in blocks. |
| HorizontalSpeed | Decimal | 0.3 | 0.0..10.0 | How fast you get pulled sideways toward the hole. |
| VerticalSpeed | Decimal | 0.1 | 0.0..10.0 | How fast you get pulled down into the hole. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/ModuleAnchor.kt)*
