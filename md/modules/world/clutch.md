## Clutch

Clutch catches you when you are about to fall deep, for example after a hit knocks you off an edge. It has [Scaffold](/docs/modules/world/scaffold) place blocks under you until you stand again. Turn it on for maps with void edges, like Bedwars or Skywars.

Scaffold does the placing, so its block, rotation and swing settings are used. Clutch does nothing while Scaffold itself is on. If a hit throws you far, it builds a row of blocks under you as you fly.

**Category:** World
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| MinFallDistance | Decimal | 5.0 | 2.0..50.0 blocks | How deep a fall has to be before Clutch catches it. Shorter falls are left alone. A fall into the void always counts. |

---
*Last updated: 2026-11-12, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/main/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/ModuleClutch.kt)*
