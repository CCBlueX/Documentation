## LiquidWalk

LiquidWalk lets you walk across the surface of water and other liquids as if they were solid ground — sometimes called the "Jesus" module. Instead of sinking or swimming, you glide across the surface at full walking speed. This is useful for crossing oceans, rivers, or any water body quickly without having to swim or build a bridge. Holding sneak (Shift) will let you sink into the water as normal when you need to dive.

The module offers four modes to help you bypass different anti-cheat systems. **Vanilla** is the simplest approach and works well on servers with no anti-cheat or very basic checks. **NoCheatPlus** and **VerusB3901** apply packet-level adjustments tailored to their respective anti-cheats. **Vulcan291** takes a different approach — when you enter water it launches you upward and briefly speeds up your tick rate, effectively skipping you across the surface; you can tune the upward **Motion** force to find the right balance between reliability and flag avoidance.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | VerusB3901 | Vanilla, NoCheatPlus, VerusB3901, Vulcan291 | Selects the liquid-walking technique. Choose the mode that matches the anti-cheat running on your server. |
| Mode → [Vulcan291] → Motion | Decimal | 0.8 | 0.2 – 1.4 | Controls the upward force applied when skipping across water in Vulcan291 mode. Lower values are more subtle; higher values propel you upward more aggressively. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/liquidwalk/ModuleLiquidWalk.kt)*
