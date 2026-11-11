## AntiBlind

AntiBlind hides effects and overlays that block your view, like Blindness, Darkness, the Nausea wobble, the carved pumpkin overlay and fog under water or lava. Turn it on when you want to see clearly.

DoRender is a list of things that stay visible. Anything you take off the list gets hidden. By default, Blindness, Darkness, Nausea, the pumpkin overlay, liquid and powder snow fog, floating items, the portal overlay and the overlay you see inside a wall are hidden. For a brighter world, use [FullBright](/docs/modules/render/fullbright).

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| DoRender | Multi-Select | Armor, MobInSpawner, EnchantTableBook, EatParticles, BlockBreakParticles, BlockBreakOverlay, Title, MapContents, MapMarkers, FallingBlocks, BeaconBeams, SkylightUpdates, GuiBackground, SpyglassOverlay, SignText, InvisibleEntities, BossBars, ExplosionParticles, WorldBorder, FallingLeaves | Blinding, Darkness, Nausea, Armor, MobInSpawner, EnchantTableBook, EatParticles, BlockBreakParticles, BlockBreakOverlay, Title, PumpkinBlur, LiquidsFog, PowderSnowFog, FloatingItems, MapContents, MapMarkers, PortalOverlay, WallOverlay, FallingBlocks, BeaconBeams, SkylightUpdates, GuiBackground, SpyglassOverlay, SignText, InvisibleEntities, BossBars, ExplosionParticles, WorldBorder, FallingLeaves | Things that are still drawn. Remove an entry to hide it. |
| FireOpacity | Integer | 100% | 0..100% | How visible the fire overlay is when you burn. Lower it to see more of the screen. |

---
*Last updated: 2026-11-11, based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/d0486b17c/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleAntiBlind.kt)*
