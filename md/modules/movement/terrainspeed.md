## TerrainSpeed

TerrainSpeed bundles movement improvements for three specific surfaces — ladders/vines, ice, and water — into a single module. Each sub-system can be toggled independently, so you can enable only the surfaces that are relevant to your situation without affecting the others.

**FastClimb** makes you ascend ladders and vines faster. The *Motion* mode applies a configurable upward velocity each tick while you're pressed against a climbable block, giving you a smooth boost that can be tuned to avoid anti-cheat flags. The *Clip* mode instead instantly teleports you to the top of the climbable section the moment you press forward — much faster, but more likely to be detected on protected servers. **IceSpeed** overrides the slipperiness of all ice variants (regular, packed, blue, and frosted), letting you control how quickly you accelerate and decelerate. Enabling its **Motion** sub-option also multiplies your horizontal momentum each tick you're on ice, so you start gliding at full pace right away.

**WaterSpeed** replaces your default swim velocity while submerged. **AutoSwim** keeps the swim-up input held automatically so you stay near the water's surface without needing to hold Jump. **BaseSpeed** sets your horizontal and vertical velocities for normal swimming, while **SprintSpeed** (active when you hold Sprint) lets you set a separate, typically higher pair of values for sprinting through water.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| FastClimb | Toggleable Group | off | — | Climb ladders and vines faster. Enable to activate the sub-settings below. |
| FastClimb → Mode | Mode Selector | Motion | — | Climbing algorithm: *Motion* applies a per-tick upward velocity (more anti-cheat friendly); *Clip* teleports you to the top of the climbable section instantly. |
| FastClimb → Mode → [Motion] → Motion | Decimal | 0.2872 | 0.1 – 0.5 | Upward velocity applied each tick while on a climbable block. Higher values climb faster. |
| IceSpeed | Toggleable Group | on | — | Modifies movement on ice blocks. Enable to activate the sub-settings below. |
| IceSpeed → Slipperiness | Decimal | 0.57 | 0.3 – 1.0 | Overrides the slipperiness of ice blocks. Lower values reduce sliding and let you control direction more easily. |
| IceSpeed → Motion | Toggleable Group | off | — | When enabled, multiplies your horizontal momentum each tick you are on ice, boosting your glide speed. |
| IceSpeed → Motion → Motion | Decimal | 0.5 | 0.2 – 1.5 | Horizontal momentum multiplier applied per tick on ice. |
| WaterSpeed | Toggleable Group | on | — | Overrides your swim velocity while submerged. Enable to activate the sub-settings below. |
| WaterSpeed → AutoSwim | Toggle | true | — | Automatically holds the swim-up input while in water so you stay near the surface without pressing Jump. |
| WaterSpeed → BaseSpeed | Setting Group | — | — | Swim speed used during normal (non-sprint) movement in water. |
| WaterSpeed → BaseSpeed → Horizontal | Decimal | 0.44 | 0.1 – 10.0 | Horizontal swim speed while not sprinting. |
| WaterSpeed → BaseSpeed → Vertical | Decimal | 0.44 | 0.1 – 10.0 | Vertical swim speed (Jump to rise, Sneak to sink) while not sprinting. |
| WaterSpeed → SprintSpeed | Toggleable Group | on | — | When enabled, uses a separate set of speeds while Sprint is held in water. |
| WaterSpeed → SprintSpeed → Horizontal | Decimal | 1.0 | 0.1 – 10.0 | Horizontal swim speed while sprinting. |
| WaterSpeed → SprintSpeed → Vertical | Decimal | 1.0 | 0.1 – 10.0 | Vertical swim speed while sprinting. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/terrainspeed/ModuleTerrainSpeed.kt)*
