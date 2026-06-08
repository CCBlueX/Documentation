## NoWeb

NoWeb prevents cobwebs from slowing you down. In vanilla Minecraft, moving through a cobweb brings your speed to a near-standstill. This module intercepts that effect and counters it according to the mode you choose, letting you pass through webs at full speed or with far less reduction.

The default **Air** mode is the most straightforward: cobwebs are treated as if they were air and impose no slowdown at all. For servers running anti-cheat software, the server-specific modes are a better fit. **Grim2365** sends block-break packets for each web you touch (and optionally removes it on your client) to satisfy Grim's movement validation. **Intave14** uses a timed pattern of strafing and jumping tuned for Intave-protected servers. **PlaceWater** takes a physical approach — when you walk into a web it automatically places a water bucket beside it to destroy the cobweb, then picks the bucket back up; this requires a water bucket in your hotbar or offhand and a world where water does not evaporate. **Strafe** applies a configurable horizontal push each tick you are inside a web and can optionally override your vertical speed as well, making it suitable for servers like Vulcan or Grim where outright cancellation would trigger flags.

Note that NoWeb is incompatible with the cobweb-avoidance behaviour of [AvoidHazards](/docs/modules/movement/avoidhazards) — if AvoidHazards has its cobweb option active when NoWeb is enabled, AvoidHazards will be automatically turned off.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Mode | Mode Selector | Air | — | Selects how cobweb slowdown is countered. Choose from Air, Grim2365, Intave14, PlaceWater, or Strafe. |
| Mode → [Grim2365] → BreakOnWorld | Toggle | true | — | Removes the cobweb block on your local client when it is broken, helping avoid the BadPacketsX check on Grim. |
| Mode → [PlaceWater] → Rotations | Setting Group | — | — | See [Shared: Rotations](/docs/modules/shared-settings/rotations). |
| Mode → [PlaceWater] → Pickup | Toggleable Group | on | — | When enabled, automatically retrieves the placed water bucket after it has had time to destroy the web. |
| Mode → [PlaceWater] → Pickup → PickupSpan | Decimal Range | 0.8..3.0 | 0.5..20.0 s | The window of time (in seconds) after placing water during which the module will attempt to pick the bucket back up. |
| Mode → [Strafe] → Strength | Decimal | 0.23 | 0.01..0.8 | The amount of horizontal strafe force applied each tick while inside a web to counteract slowdown. |
| Mode → [Strafe] → MotionY | Toggleable Group | off | — | When enabled, overrides your vertical velocity while inside a web. |
| Mode → [Strafe] → MotionY → MotionYStrength | Decimal | 0.6 | -2.0..2.0 | The vertical speed set while inside a web. Positive values push you upward; negative values push you downward. |
| Mode → [Strafe] → OnlyOnGround | Toggle | false | — | Restricts the strafe force to only apply when you are standing on the ground. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/noweb/ModuleNoWeb.kt)*
