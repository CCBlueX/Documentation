## TNTTimer

TNTTimer highlights active (primed) TNT entities in the world so you can track them at a glance. When TNT is ignited, it counts down for 80 ticks (4 seconds) before exploding — this module makes it easy to see exactly which TNT blocks are live and how close they are to detonating, which is especially useful in PvP scenarios involving [CrystalAura](/docs/modules/combat/crystalaura) or cannon-based combat where multiple TNT entities may be active simultaneously.

With **ESP** enabled, each primed TNT is visually highlighted using a pulsing red glow that cycles faster as the fuse runs out, giving you an immediate sense of urgency. Optionally, the **ShowTimer** group overlays a countdown label directly on each TNT in the world, transitioning from yellow to red as the fuse nears zero. You can also display the name of the player who ignited each TNT, which is useful for identifying who is running a cannon or placing explosives nearby.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| ESP | Toggle | true | — | Highlights primed TNT entities with a pulsing ESP glow that cycles faster the shorter the remaining fuse. |
| ShowTimer | Toggleable Group | off | — | When enabled, displays a countdown label above each primed TNT in the world. |
| ShowTimer → Scale | Decimal | 1.5 | 0.25 – 4.0 | Controls the size of the countdown label rendered above each TNT. |
| ShowTimer → RenderY | Decimal | 1.0 | -2.0 – 2.0 | Vertical offset of the countdown label relative to the TNT's centre. Negative values move the label downward. |
| ShowTimer → OwnerName | Toggle | true | — | Appends the name of the player who ignited the TNT to the countdown label, e.g. `20 (Steve)`. |
| ShowTimer → TimeUnit | Choice | Ticks | — | Determines whether the countdown is shown in ticks or seconds. **Ticks** shows a whole-number countdown (80 → 0); **Seconds** shows a decimal value (e.g. `1.00s`). |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleTNTTimer.kt)*
