## AntiBlind

AntiBlind cleans up your screen by hiding the visual effects and overlays that can get in the way during gameplay — things like the blindness and darkness effects, the nausea (portal) wobble, the pumpkin blur when wearing a carved pumpkin, fog from liquids and powder snow, and full-screen overlays from portals or clipping into walls. Many of these are blocked by default, so the moment you enable the module your view becomes a lot clearer.

The **DoRender** setting works as a "keep visible" list: every entry you leave enabled stays rendered as normal, while anything you remove from the list gets hidden. To block an annoying effect, take it off the list; to bring something back, add it again. By default the list keeps useful visuals (armor, sign text, boss bars, map contents, and similar) while leaving the disorienting effects switched off. If you want permanent map-wide brightness instead, pair this with [FullBright](/docs/modules/render/fullbright).

**FireOpacity** controls how see-through the fire overlay is when you catch fire. Lower values fade the flames out of your view so they don't block your screen, while 100% leaves them fully visible.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| DoRender | Multi-Select | Armor, MobInSpawner, EnchantTableBook, EatParticles, BlockBreakParticles, BlockBreakOverlay, Title, MapContents, MapMarkers, FallingBlocks, BeaconBeams, SkylightUpdates, GuiBackground, SpyglassOverlay, SignText, InvisibleEntities, BossBars, ExplosionParticles | Blinding, Darkness, Nausea, Armor, MobInSpawner, EnchantTableBook, EatParticles, BlockBreakParticles, BlockBreakOverlay, Title, PumpkinBlur, LiquidsFog, PowderSnowFog, FloatingItems, MapContents, MapMarkers, PortalOverlay, WallOverlay, FallingBlocks, BeaconBeams, SkylightUpdates, GuiBackground, SpyglassOverlay, SignText, InvisibleEntities, BossBars, ExplosionParticles, WorldBorder | Choose which effects and overlays stay visible. Anything left enabled renders normally; anything removed is hidden. |
| FireOpacity | Integer | 20% | 0–100% | How visible the fire overlay is when you're burning. Lower values fade the flames so they obscure less of your screen. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleAntiBlind.kt)*
