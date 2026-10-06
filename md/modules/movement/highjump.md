## HighJump

HighJump lets you leap higher than the normal Minecraft jump, boosting your upward launch the moment you press jump. It's handy for reaching ledges, scaling walls, or clearing obstacles that a standard jump can't get you over.

Pick a **Mode** based on the server you're on. **Vanilla** simply replaces your jump with a stronger one and works best on unprotected servers. **Vulcan** is tuned to slip past the Vulcan anticheat and adds an optional **Glide** behavior that smooths your descent so the bigger jump looks less suspicious. The **Motion** value controls how strong the launch is — higher means more height. For more movement tricks, see [LongJump](/docs/modules/movement/longjump), [Step](/docs/modules/movement/step), and [AirJump](/docs/modules/movement/airjump).

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Vanilla | Vanilla, Vulcan | Chooses how the high jump is performed. Vanilla for unprotected servers; Vulcan to evade the Vulcan anticheat. |
| Mode → [Vulcan] → Glide | Toggle | false | — | When using the Vulcan mode, eases your descent after the jump for a smoother, less detectable fall. |
| Motion | Decimal | 0.44 | 0.2..10.0 | How much upward force is applied when you jump. Higher values launch you higher. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/highjump/ModuleHighJump.kt)*
