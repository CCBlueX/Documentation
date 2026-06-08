## AutoWalk

AutoWalk is the shared movement engine that lets a module automatically walk your character toward a chosen spot or target. Instead of you holding the movement keys, the module hands AutoWalk a destination and it steers you there — picking a route, moving forward, and deciding which movement tricks (like jumping or swimming) it's allowed to use along the way. When the module no longer has a destination, AutoWalk simply stops moving you.

The settings here control *how* that walking behaves: which movement abilities are permitted, how close you need to get before AutoWalk considers you "arrived," and (for farming-style use) whether it should also route you to blocks that need replanting and to dropped items worth picking up. Because it's shared, the exact relevance of some options depends on the module using it — for example, the planting and item-pickup options matter most for [AutoFarm](/docs/modules/world/autofarm), while [FreeCam](/docs/modules/render/freecam) and [KillAura](/docs/modules/combat/killaura) mainly use the core walking and distance behavior.

Tune these if AutoWalk is overshooting its target, refusing to cross water, or wandering off to grab items you don't want.

This setting group is used by the following modules:

- [AutoFarm](/docs/modules/world/autofarm)
- [FreeCam](/docs/modules/render/freecam)
- [KillAura](/docs/modules/combat/killaura)

### Settings

| Setting | Type | Default | Range | Description |
| --- | --- | --- | --- | --- |
| Auto | Multi-Select | Jump, Swim, Sprint | — | Which movement abilities AutoWalk is allowed to use while pathing to its destination. **Jump** lets it hop over obstacles and ledges, **Swim** lets it move up and through water, and **Sprint** lets it run for faster travel. Turn off any you'd rather it avoid. |
| MinimumDistance | Decimal | 2.0 | 1.0–4.0 | How close (in blocks) you need to get to the destination before AutoWalk counts it as reached and stops moving you. Lower values bring you right up to the spot; higher values stop you a bit further away. |
| ToPlant | Toggle | true | — | When enabled, AutoWalk will also route you to empty farmland or soul sand that needs a crop replanted, as long as you're carrying suitable planting items. With it off, it only heads toward blocks that are ready to be harvested or broken. |
| ToItems | Toggleable Group | On | — | When enabled, AutoWalk will also walk over to nearby dropped items to pick them up (skipped if your inventory is full). Turn the whole group off to ignore loot and only path to blocks. |
| ToItems → Range | Decimal | 20.0 | 8.0–64.0 | How far away (in blocks) a dropped item can be for AutoWalk to consider going after it. |
| ToItems → Items | Registry List | — | — | The list of item types used together with the Filter option to decide which dropped items AutoWalk will go pick up. |
| ToItems → Filter | Choice | Blacklist | — | How the Items list is applied. **Blacklist** picks up everything *except* the listed items; **Whitelist** picks up *only* the listed items. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/world/autofarm/AutoFarmAutoWalk.kt)*
