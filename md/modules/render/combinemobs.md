## CombineMobs

CombineMobs cleans up your view when lots of entities of the same type are packed into the same spot. Instead of drawing every crammed mob on top of one another, it renders a single entity and shows a count of how many are grouped together. This is great for high-traffic servers and old anarchy spawns (like 2b2t) where huge stacks of mobs cause clutter and frame drops.

By default it works on living mobs (animals and monsters). Baby and adult mobs are kept in separate groups, so a stack of chickens won't be merged with a stack of baby chickens. If you also want to fold together armor stands or minecarts that pile up in the same place, enable the matching options below.

**Category:** Render
**Enabled by default:** No

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| CombineArmorStands | Toggle | false | — | Also combines armor stands that are crammed together into a single rendered stand with a count. |
| CombineMinecarts | Toggle | false | — | Also combines minecarts that are crammed together into a single rendered minecart with a count. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleCombineMobs.kt)*
