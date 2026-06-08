## TrueSight

TrueSight reveals hidden objects and entities that would otherwise be invisible to you. With it enabled, barrier blocks — the normally completely transparent and undetectable blocks that servers use as invisible walls — become visible, and invisible entities (players, mobs, or other creatures affected by the Invisibility effect) are rendered so you can see and track them.

By default both detection types are active, making TrueSight useful in a wide variety of situations: finding hidden arena boundaries, spotting invisible players sneaking up on you in PvP, or locating invisible mobs. TrueSight also works together with [ESP](/docs/modules/render/esp) — if ESP needs to highlight an invisible entity, TrueSight's rendering logic is used automatically even when the entity sight option here is off.

The two color settings let you control exactly how invisible entities appear. `EntityColor` sets the tint applied to the entity's main body when rendered through TrueSight, while `EntityFeatureLayerColor` controls the color of secondary render layers (such as armor or worn items). Adjusting the alpha (opacity) of these colors is the easiest way to make ghostly entities more or less prominent on your screen.

**Category:** Render
**Enabled by default:** Yes

### Settings

| Setting | Type | Default | Range | Description |
|---|---|---|---|---|
| Sight | Multi-Select | Barriers, Entities | Barriers, Entities | Choose which invisible things to reveal: barrier blocks, invisible entities, or both. |
| EntityColor | Color | — | — | Tint color applied to the body of invisible entities when they are revealed. |
| EntityFeatureLayerColor | Color | — | — | Tint color applied to secondary render layers (e.g. armor) of invisible entities. |

---
*Last updated: 2026-06-08 — Based on [source code](https://github.com/CCBlueX/LiquidBounce/blob/2b0edfcf2/src/main/kotlin/net/ccbluex/liquidbounce/features/module/modules/render/ModuleTrueSight.kt)*
