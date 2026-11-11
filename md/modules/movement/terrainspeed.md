## TerrainSpeed

TerrainSpeed makes you faster on ladders and vines, on ice, and in water. Each part has its own group, so you can turn on only the ones you want.

FastClimb gets you up ladders and vines faster. Motion mode pushes you up a bit faster every tick. Clip mode puts you at the top of the ladder right away, which is quicker but easier for anti-cheats to spot. IceSpeed changes how slippery all kinds of ice are. WaterSpeed sets how fast you swim, with a second, faster speed while you hold sprint.

**Category:** Movement
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| FastClimb | Toggleable Group | on | | Climb ladders and vines faster. |
| FastClimb → Mode | Mode Selector | Motion | Motion, Clip | Motion climbs faster. Clip puts you at the top right away. |
| FastClimb → Mode → [Motion] → Motion | Decimal | 0.2872 | 0.1..0.5 | How fast you climb. |
| IceSpeed | Toggleable Group | on | | Changes how you move on ice. |
| IceSpeed → Slipperiness | Decimal | 0.6 | 0.3..1.0 | How slippery ice is. Lower means less sliding and easier turning. |
| IceSpeed → Motion | Toggleable Group | off | | Changes your speed on ice. |
| IceSpeed → Motion → Motion | Decimal | 0.5 | 0.2..1.5 | Speed multiplier on ice. |
| WaterSpeed | Toggleable Group | on | | Sets how fast you swim. |
| WaterSpeed → AutoSwim | Toggle | true | | Swims up for you so you stay near the surface without holding jump. |
| WaterSpeed → BaseSpeed → Horizontal | Decimal | 0.44 | 0.1..10.0 | Swim speed forward and sideways. |
| WaterSpeed → BaseSpeed → Vertical | Decimal | 0.44 | 0.1..10.0 | Swim speed up (jump) and down (sneak). |
| WaterSpeed → SprintSpeed | Toggleable Group | on | | Uses the speeds below while you hold sprint. |
| WaterSpeed → SprintSpeed → Horizontal | Decimal | 1.0 | 0.1..10.0 | Swim speed forward and sideways while sprinting. |
| WaterSpeed → SprintSpeed → Vertical | Decimal | 1.0 | 0.1..10.0 | Swim speed up and down while sprinting. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/movement/terrainspeed/ModuleTerrainSpeed.kt)*
